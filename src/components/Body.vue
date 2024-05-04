<template>
  <div class="bodyContainer">
    <OtherTableThing />
  </div>
</template>

<script lang="ts">
import { defineComponent } from "vue";
import OtherTableThing from "./OtherTableThing.vue";

export default defineComponent({
  name: "App",
  components: {
    OtherTableThing,
  },
});
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  // text-align: center;
  // background-color: #2c3e50;
  //   background-color: "#ffffff";
}

// body {
//   margin: 0; // background-color: #2c3e50;
// }
.bodyContainer {
  display: flex;
  border: solid;

  border-width: 5px;
  border-color: green;
  justify-content: center;
  // background-color: #7BC4E0;
  background-color: rgb(37, 150, 190, 0.3);
  // opacity: 0.3;
}
</style>