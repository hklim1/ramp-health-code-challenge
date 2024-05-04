<template>
  <Navbar />

  <Body />
</template>

<script lang="ts">
import { defineComponent } from "vue";
import Navbar from "./components/Navbar.vue";
import Body from "./components/Body.vue";

export default defineComponent({
  name: "App",
  components: {
    Navbar,
    Body,
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
    // color: #2c3e50;
    background-color: "#ffffff";
  }
  
  body {
    margin: 0; // background-color: #2c3e50;
  }
</style>
