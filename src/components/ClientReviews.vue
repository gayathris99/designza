<template>
  <div class="background-grey q-pa-lg ">
  <div class="fs-36 color-brown" :class="isDesktop ? 'q-pa-md' : ''">
    <div class="fw-500">WHAT OUR CLIENTS</div>
    <div class="fw-900">HAVE TO SAY</div>
    <div class="color-orange row items-center align-center q-mt-sm q-mb-md">
      <template v-for="i in 5" :key="i">
        <q-icon name="star" size="sm"/>
      </template>
      <div class="color-brown fs-16 q-pl-sm fw-500">BASED ON 300+ REVIEWS</div>
    </div>
      <!-- Reviews Section -->
    <q-carousel
      swipeable
      animated
      v-model="slide"
      :autoplay="autoplay"
      ref="carousel"
      infinite
      class="bg-rounded"
    >
      <q-carousel-slide :name="1">
        <div class="row justify-center">
          <q-card rounded class="q-pa-md">
            <div class="row items-center justify-evenly">
              <div class="col-md-6 col-sm-12 col-xs-12 image-container">
                <img src="~assets/stepimage.jpg" alt="">
              </div>
              <div class="col-md-6 col-sm-12 col-xs-12">
                <div class="fs-20 fw-600">John Doe</div>
                <div class="fs-16 color-grey fw-500">Kitchen Redesign, Bangalore</div>
                <div class="q-mt-md fs-18">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Reprehenderit, maxime autem. Ad adipisci aspernatur, quo recusandae sit incidunt sequi deleniti numquam culpa asperiores vero sapiente? Porro quasi ad obcaecati aliquam.
                </div>
              </div>
            </div>
          </q-card>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2">
        <div class="row justify-center">
          <q-card rounded class="q-pa-md">
            <div class="row items-center justify-evenly">
              <div class="col-md-6 col-sm-12 col-xs-12 image-container">
                <img src="~assets/stepimage2.jpg" alt="">
              </div>
              <div class="col-md-6 col-sm-12 col-xs-12">
                <div class="fs-20 fw-600">Mary Doe</div>
                <div class="fs-16 color-grey fw-500">Kitchen Redesign, Bangalore</div>
                <div class="q-mt-md fs-18">
                  Lorem ipsum dolor sit amet consectetur adipisicing elit. Repellendus deleniti praesentium neque cumque tempore expedita totam, iure ex maiores quis excepturi blanditiis nostrum ducimus quo libero in officia nihil enim!
                </div>
              </div>
            </div>
          </q-card>
        </div>
      </q-carousel-slide>
      <!-- <q-carousel-slide :name="2" img-src="https://cdn.quasar.dev/img/parallax1.jpg" /> -->
      <template v-slot:control>
        <q-carousel-control
          position="bottom-right"
          :offset="[18, 18]"
          class="q-gutter-xs"
        >
          <q-btn
            push round dense color="orange" text-color="black" icon="arrow_left"
            @click="$refs.carousel.previous()"
          />
          <q-btn
            push round dense color="orange" text-color="black" icon="arrow_right"
            @click="$refs.carousel.next()"
          />
        </q-carousel-control>
      </template>
    </q-carousel>
  </div>
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'ClientReviews',
  setup () {
      return {
        slide: ref(1),
        autoplay: ref(true)
      }
    },
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
.q-carousel {
  background-color: #f9f9f9;
}
.q-card {
  max-width: 60vw;
  box-shadow: none !important;
  @media only screen and (max-width: $breakpoint-sm-max) {
    max-width: 90vw;
  }
  @media only screen and (max-width: $breakpoint-xs-max) {
    width: auto;
  }
}
.image-container {
  img {
    width: 90%;
    // max-height: 200px;
    object-fit: cover;
    border-radius: 20px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  @media only screen and (max-width: $breakpoint-sm-max) {
    width: 95%;
  display: block;
  margin-left: auto;
  margin-right: auto;
  margin-bottom: 30px;
  }
  }
}
</style>
