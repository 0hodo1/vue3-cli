<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <br />
  <Header :title="word" @clear="sil" />
  <input ref="text" />
  <br />
  <h1>CLI Projects</h1>
  <!-- <input type="text" ref="name" />
  <input type="text" ref="password" />
  <button @click="handleClick()">Click</button> -->
  <br />
  <Form />
</template>

<script>
import Header from "./components/Header.vue";
import Form from "./components/Form.vue";

export default {
  name: "App",
  data() {
    return {
      word: "Hello Vue3",
    };
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name.value);
      console.log(this.$refs.password.value);
    },
    sil() {
      this.$refs.text.value = "";
    },
  },
  components: {
    Header,
    Form,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
