<template>
  <div class="background-grey q-pa-lg">
    <div class="row items-center justify-around color-brown" :class="isDesktop ? 'q-pa-md' : ''">
      <div class="col-md-6 col-sm-12 col-xs-12">
        <div class="fs-28">
          <span class="fw-600">FOOTPRINT OF &nbsp;</span>
          <br/>
          <span class="fw-900">SUCCESS STORIES</span>
        </div>
        <div class="col-md-6 col-sm-12 col-xs-12 q-pt-md">
          <img src="~assets/herobanner.jpg" alt="">
        </div>
      </div>
      <div class="col-md-6 col-sm-12 col-xs-12">
        <div class="fs-16 q-mt-md">
          Lorem ipsum dolor, sit amet consectetur adipisicing elit. Aliquam perspiciatis, quasi, dignissimos alias, magni dolor illo nemo at reiciendis recusandae vel commodi illum ad quibusdam quisquam minima magnam voluptates incidunt!
        </div>
        <div>
          <div class="row items-center q-gutter-x-xl q-mt-md" :class="isTablet ? 'align-center justify-center': 'justify-start'">
            <div>
              <div class="fw-900 fs-48">40+</div>
              <div>OUR PRODUCTS</div>
            </div>
            <div>
              <div class="fw-900 fs-48">5+</div>
              <div>EXPERIENCE YEARS</div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'SuccessStories',
  computed: {
    isTablet () {
      return this.$q.screen.gt.xs && this.$q.screen.lt.md
    },
    isDesktop () {
      return this.$q.screen.gt.sm
    }
  }
}
</script>

<style lang="scss" scoped>
img {
  width: 40vw;
  height: 200px;
  object-fit: cover;
  border-radius: 50px;
    @media only screen and (max-width: $breakpoint-sm-max) {
      width: 90vw;
    }
    @media only screen and (max-width: $breakpoint-xs-max) {
      width: 85vw;
    }
}
</style>
