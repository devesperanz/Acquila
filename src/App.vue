<template>
  <div>
    <Main />
    <!-- <router-view /> -->
  </div>
</template>

<script>
import Main from "./components/Main.vue";
export default {
  name: "App",
  components: {
    Main,
  },
};
</script>
<style>
@import url("https://fonts.googleapis.com/css2?family=Julius+Sans+One&display=swap");
#nav {
  padding: 50px;
}

#nav a {
  color: rgba(255, 255, 255, 0.774);
  text-decoration: none;
  letter-spacing: 8px;
  font-weight: 100;
}

#nav a.router-link-exact-active {
  color: #fff;
}
</style>
