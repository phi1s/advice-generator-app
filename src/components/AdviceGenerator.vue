<template>
  <div class="AdviceGenerator">
    <h1>Advice #{{ slip.id }}</h1>
    <p>"{{ slip.advice }}"</p>
    <div class="divider" />
    <button class="dice" @click="getAdvice()">
      <img src="../assets/icon-dice.svg" alt="icon dice" />
    </button>
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
  width: 343px;
  height: 315px;
  background-color: #313a48;
  position: relative;
  border-radius: 10px;
}

button:hover {
  box-shadow: 0px 0px 40px #53ffaa;
}
.divider {
  width: 295px;
  height: 16px;
  margin: auto;
  background-image: url("../assets/pattern-divider-mobile.svg");
}
.dice {
  width: 64px;
  height: 64px;
  border-radius: 50%;
  background-color: #53ffaa;
  position: absolute;
  left: calc(50% - 32px);
  bottom: -32px;
}
img {
  padding: 20px;
}

button {
  border: none;
  padding: 0;
}

@media screen and (min-width: 700px) {
  .AdviceGenerator {
    width: 540px;
    height: 332px;
  }
  .divider {
    width: 444px;
    height: 16px;
    background-image: url("../assets/pattern-divider-desktop.svg");
  }
}
</style>
