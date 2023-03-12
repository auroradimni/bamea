<template>
  <div class="about">
    <h3 class="title">About us</h3>
    <div>
      <p>
        Hello everyone, in this blog we want to share our thoughts and experiences with you, the
        topics we will mostly talk about are: technology, lifestyle, books, social media, etc.We
        hope you enjoy your free time reading our articles.
      </p>
      <div class="image-holder">
        <img src="../assets/download.webp" alt="logo" />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {}
  }
}
</script>

<style scoped>
.about {
  box-shadow: 0 5px 10px 0 rgb(24, 120, 120);
  max-width: 600px;
  margin: auto;
  text-align: center;
  font-family: arial;

  height: 400px;
  right: 0%;
  left: 0%;
  padding: 50px;
  position: fixed;
  top: 100px;
}
.title {
  text-align: center;
  color: rgb(24, 120, 120);
  font-style: italic;
  font-family: cursive;
}
.image-holder {
  object-fit: scale-down;
  max-width: 300px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  bottom: auto;
}
.image-holder img {
  object-fit: scale-down;
  max-width: 200px;
}
</style>
