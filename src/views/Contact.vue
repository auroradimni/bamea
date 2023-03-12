<template>
  <div class="contact">
    <h3 class="title">Contact us</h3>
    <div>
      <div class="image-holder">
        <img src="../assets/download.webp" alt="logo" />
      </div>
    </div>

    <div class="icon-holder">
      <a href=""> <img class="icons" src="../assets/ig.jpg" alt="instagram" /></a>
      <a href=""><img class="icons" src="../assets/pi.png" alt="pinterest" /></a>
      <a href=""><img class="icons" src="../assets/li.png" alt="linkedin" /></a>
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
.contact {
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
.icon-holder {
  display: flex;
  gap: 5%;
  left: 0;
  right: 0;
}
.icons {
  max-width: 30%;
  max-height: 50%;
  object-fit: scale-down;
  bottom: 0%;
}
</style>
