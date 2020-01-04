<template>
  <div id="app">
    <h1 style="font-size:24px;">いめーじめーかー for 年賀状</h1>
    <img alt="Vue logo" src="./assets/mark_onenga.png" />
    <Hello />
  </div>
</template>

<script>
import Hello from "./components/Hello.vue";

export default {
  name: "app",
  components: {
    Hello
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1 {
  font-size: 24px;
}
</style>
