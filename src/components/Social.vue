<template>
  <div>
    <img src="../assets/Bg_img.png" alt="" class="bgimg" />
    <span>
      <a :href="`https://www.instagram.com/${title.instagram}`">
        <i class="fa fa-instagram" aria-hidden="true"></i>
      </a>
      <a :href="`https://www.twitter.com/${title.twitter}`">
        <i class="fa fa-twitter-square" aria-hidden="true"></i>
      </a>
      <a :href="`https://www.snapchat.com/${title.snapchat}`">
        <i class="fa fa-snapchat-square" aria-hidden="true"></i>
      </a>
      <a :href="`mailto:${title.email}`">
        <i class="fa fa-envelope-square" aria-hidden="true"></i>
      </a>
    </span>
  </div>
</template>

<script>
export default {
  props: ["title"],
};
</script>

<style scoped>
span {
  position: fixed;
  top: 180px;
  right: 10px;
}
span i {
  display: block;
  margin: 30px;
  font-size: 1.6rem;
}
span a {
  text-decoration: none;
  color: #fff;
}
.bgimg {
  width: 50%;
  max-width: 100%;
  box-shadow: -8px 8px 40px 0px rgb(105, 104, 104, 0.4);
}
</style>