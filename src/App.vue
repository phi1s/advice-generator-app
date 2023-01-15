<template>
  <AdviceGenerator />
</template>

<script>
import AdviceGenerator from "./components/AdviceGenerator.vue";

export default {
  name: "App",
  components: {
    AdviceGenerator,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #cee3e9;
  background-color: #202733;
  text-align: center;
  position: absolute;
  top: 0;
  left: 0;
  width: 100vw;
  height: 100vh;
  overflow: hidden;
  display: flex;
  justify-content: center;
  align-items: center;
}
h1 {
  color: #53ffaa;
}
</style>
