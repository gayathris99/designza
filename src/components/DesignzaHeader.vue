<template>
  <div class="row items-center q-gutter-sm cursor-pointer q-pa-md font-mona header background-grey"  @click="goToHomePage">
      <img src="~assets/designza_logo.png" alt="Designza Logo" width="40">
      <div class="fw-700 fs-20 color-brown">Designza Home Interiors</div>
  </div>
 <!-- <div class="row q-pa-md align-center items-center q-gutter-sm font-crimson justify-between">
    <div class="items-center row q-gutter-sm cursor-pointer" @click="goToHomePage">
      <img src="~assets/designza_logo.png" alt="Designza Logo" width="50">
      <div class="fs-28 fw-700">Designza Home Interiors</div>
    </div>
    <div v-if="isDesktop" class="row items-center q-gutter-sm">
      <div class="row items-center q-gutter-lg font-worksans fw-400 fs-20">
        <div class="cursor-pointer">Services</div>
        <div class="cursor-pointer">Portfolio</div>
        <div class="cursor-pointer">Contact Us</div>
      </div>
    </div>
  </div> -->
</template>

<script>
export default {
  name: 'DesignzaHeader',
  methods: {
    goToHomePage () {
      this.$router.push({ name: 'Homepage' })
    }
  },
  computed: {
    isMobile () {
      return this.$q.screen.lt.sm
    },
    isTablet () {
      return this.$q.screen.gt.xs && this.$q.screen.lt.md
    },
    isDesktop () {
      return this.$q.screen.gt.sm
    },
  }

}
</script>

<style lang="scss" scoped>
.header {
  position: sticky;
  top: 0;
  width: 100%;
  z-index: 999;
}
</style>
