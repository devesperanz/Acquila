<template>
  <header class="header">
    <h1>{{ title.name }}</h1>
    <Social v-bind:title="title.social_media" />
    <div id="nav">
      <ul>
        <router-link to="/">
          <li>Home</li>
        </router-link>
        <router-link to="/about">
          <li>About</li>
        </router-link>
        <router-link to="#">
          <li><img src="../assets/navimg.jpg" alt="" class="navimg" /></li>
        </router-link>
        <router-link to="/gallery">
          <li>Gallery</li>
        </router-link>
        <router-link to="/contact">
          <li>Contact</li>
        </router-link>
      </ul>
    </div>
  </header>
</template>

<script>
import axios from "axios";
import Social from "./Social";
export default {
  components: {
    Social,
  },
  data() {
    return {
      title: {
        social_media: {},
      },
    };
  },
  created() {
    axios
      .get("https://hirng-x2021.glitch.me/api")
      .then((res) => (this.title = res.data))
      .catch((err) => console.log(err));
  },
};
</script>

<style scoped>
header {
  background: linear-gradient(to right, #bd0f4d 50%, #cb2964 10%);
  min-height: 100vh;
  text-align: center;
  color: rgba(255, 255, 255, 0.774);
  padding-top: 30px;
}
.header h1 {
  font-weight: 100;
  font-size: 40px;
  letter-spacing: 8px;
  padding-bottom: 30px;
}
.navimg {
  width: 5em;
  height: 5em;
  border-radius: 50%;
}
ul {
  padding: 0 20% 0 26%;
  list-style-type: none;
  display: flex;
  justify-content: space-around;
  align-items: center;
  font-weight: 100;
}
li {
  list-style: none;
  display: inline;
  padding: 20px;
}
@media (max-width: 768px) {
  ul {
    display: block;
    padding: 0;
    justify-content: space-around;
    align-items: center;
    font-weight: 100;
  }
  ul li {
    margin-bottom: 10px;
    display: block;
    padding: 10px;
  }
  .header h1 {
    font-size: 30px;
    letter-spacing: 3px;
  }
}
</style>