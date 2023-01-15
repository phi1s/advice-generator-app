<template>
  <div class="AdviceGenerator">
    <h1>Advice #{{ slip.id }}</h1>
    <p>{{ slip.advice }}</p>
    <button @click="getAdvice()">shuffle</button>
  </div>
</template>

<script>
import axios from "axios";
export default {
  name: "AdviceGernerator",
  data() {
    return {
      slip: {},
    };
  },
  mounted() {
    this.getAdvice();
  },

  methods: {
    getAdvice() {
      axios
        .get("https://api.adviceslip.com/advice")
        .then((response) => (this.slip = response.data.slip))
        .catch((err) => {
          // Handle errors
          console.error(err);
        });
    },
  },
};
</script>

<style scoped>
.AdviceGenerator {
  width: 540px;
  height: 332px;
  background-color: #313a48;
}
</style>
