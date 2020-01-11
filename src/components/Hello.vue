<template>
  <div class="hello">
    <h1 style="margin:20px;">テンプレート通りはイヤだけど簡単に年賀状イラストを作りたい人のためのサービスです</h1>
    <p>
      <a>
        <b-button type="is-info" @click="pjtStart">はじめる</b-button>
      </a>
    </p>
  </div>
</template>

<script>
export default {
  name: "Hello",
  methods: {
    pjtStart() {
      this.$emit("click");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
