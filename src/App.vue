<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <header-app ref="header" />
  <HelloWorld ref="hello" msg="Welcome to Your Vue.js App" />
  <button @click="onChange">Click me</button>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import Header from "./components/Header.vue";

export default {
  name: "App",
  components: {
    HelloWorld,
    HeaderApp: Header,
  },
  methods: {
    onChange() {
      console.log("...running here");
      console.log(this.$refs.header);
      console.log(this.$refs.hello);
    },
  },
};
</script>
