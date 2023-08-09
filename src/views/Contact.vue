<template>
  <div class="contact">
    <h3 class="title">Contact us</h3>
    <div>
      <h1 class="logo1 color-primary">Bamea</h1>
      <p class="moto1 color-black">good things take time</p>
    </div>

    <div class="icon-holder">
      <a href=""> <img class="icons" src="@/assets/ig.jpg" alt="instagram" /></a>
      <a href=""><img class="icons" src="@/assets/pi.png" alt="pinterest" /></a>
      <a href=""><img class="icons" src="@/assets/li.png" alt="linkedin" /></a>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {}
  }
}
</script>

<style scoped lang="scss">
.contact {
  box-shadow: 0 5px 10px mapget($colors, 'primary');
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
  color: mapget($colors, 'primary');
  font-style: normal;
  font-family: 'Segoe Script';
}
.image-holder {
  object-fit: scale-down;
  max-width: 300px;
  display: block;
  margin-left: auto;
  margin-right: auto;
  bottom: auto;
}

.icon-holder {
  display: flex;
  gap: 5%;
  left: 0;
  right: 0;
}
.icons {
  max-width: 50%;
  max-height: 70%;
  object-fit: scale-down;
  bottom: -70%;
}
</style>
