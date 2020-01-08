<template>
  <div id="app">
    <h1 style="font-size:24px; cursor: pointer;" @click="home = true">いめーじめーかー for 年賀状</h1>
    <img v-if="home" alt="Vue logo" src="./assets/mark_onenga.png" />
    <Hello v-if="home" @click="stateChange" />
    <card-editor v-if="!home"></card-editor>
  </div>
</template>

<script>
import Hello from "./components/Hello.vue";
import cardEditor from "./components/card-editor.vue";
export default {
  name: "app",
  components: {
    Hello,
    cardEditor
  },
  data: function() {
    return {
      home: true
    };
  },
  methods: {
    stateChange() {
      if (this.home) {
        this.home = false;
      }
    }
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
  max-height: 100%;
}
h1 {
  font-size: 24px;
}
</style>
