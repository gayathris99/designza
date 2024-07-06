<template>
  <router-view />
  <a href="https://wa.me/918892777709" target="_blank">
    <div class="logo">
      <img src="~assets/whatsapp.png" alt="">
    </div>
  </a>
</template>

<script setup>
defineOptions({
  name: 'App'
});
</script>
<style lang="scss" scoped>
.logo {
  position: fixed;
  bottom: 30px;
  right: 20px;
  img {
    width: 40px;
  }
  @media only screen and (max-width: $breakpoint-xs-max) {
bottom: 10px;
  }
}
</style>
