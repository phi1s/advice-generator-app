<template>
  <link rel="preconnect" href="https://fonts.googleapis.com" />
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin />
  <link
    href="https://fonts.googleapis.com/css2?family=Manrope:wght@800&display=swap"
    rel="stylesheet"
  />
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
  font-family: "Manrope", sans-serif;
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
  font-family: "Manrope";
  font-style: normal;
  font-weight: 800;
  font-size: 13px;
  line-height: 18px;
  text-align: center;
  letter-spacing: 4.08571px;
  color: #53ffaa;
  size: 13px;
  text-transform: uppercase;
  margin-top: 40px;
}

p {
  font-family: "Manrope";
  font-style: normal;
  font-weight: 800;
  font-size: 24px;
  line-height: 33px;
  text-align: center;
  letter-spacing: -0.257143px;
  color: #cee3e9;
  padding: 0px 14px;
}

@media screen and (min-width: 700px) {
  p {
    font-size: 28px;
    line-height: 38px;
    letter-spacing: -0.3px;
    margin-bottom: 40px;
  }
}
</style>
