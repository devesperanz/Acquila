<template>
  <div id="app">
    <Home />
  </div>
</template>

<script>
import Home from "./Home.vue";

export default {
  name: "App",
  components: {
    Home,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: "Julius Sans One", sans-serif;
}
</style>
