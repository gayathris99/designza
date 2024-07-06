<template>
  <div class="q-pa-md background-grey font-mona">
    <div class="q-pa-xl q-mx-xl container column align-center justify-center items-center">
      <div class="color-brown fw-700 fs-52 text-left row items-center q-gutter-x-lg">
        <div>THE ART</div>
        <div class="fw-400 fs-16 subtitle">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquam perspiciatis, quasi, dignissimos alias, e </div>
      </div>
      <div class="fs-52 text-center">
        <span class="color-brown fw-700">OF </span>
        <span class="color-orange fw-900">INTERIOR DESIGN!</span>
      </div>
    </div>
  </div>
        <!-- // <div class="color-orange fw-700 fs-48 text-center"><span class="color-brown">OF</span> INTERIOR</div>
      // <div class="color-brown fw-700 fs-48 text-right">DESIGN!</div> -->
</template>
<script>
export default {
  name: 'HeroBanner'
}
</script>

<style lang="scss" scoped>
.subtitle {
  max-width: 30vw;
}
img {
  // width: 40vw;
  // max-width: 720px;
  height: 120px;
  object-fit: cover;
  border-radius: 50px;
    // @media only screen and (max-width: $breakpoint-sm-max) {
    //   width: 90vw;
    // }
    // @media only screen and (max-width: $breakpoint-xs-max) {
    //   width: 85vw;
    // }
}
</style>
