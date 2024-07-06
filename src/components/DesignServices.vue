<template>
  <div class="q-pa-lg">
    <div class="color-brown" :class="isDesktop ? 'q-pa-md fs-36' : 'fs-32'">
      <div class="fw-700">COMPREHENSIVE INTERIOR</div>
      <div class="fw-900">DESIGN SERVICES</div>
      <div class="q-mt-md">
    <q-carousel
      v-model="slide"
      animated
      ref="carousel"
      swipeable
      :autoplay="autoplay"
      height="500px"
    >
      <template v-if="isDesktop">
      <q-carousel-slide :name="1" class="column no-wrap" >
        <div class="row fit justify-start items-center q-gutter-md q-col-gutter no-wrap color-brown">
          <div class="col-4 image-container column items-center">
            <img src="~assets/kitchen.jpg" alt="" srcset="">
            <div class="text-center fs-18 fw-500 q-mt-sm">Kitchen Interiors</div>
          </div>
          <div class="col-4 image-container column items-center">
            <img src="~assets/livingarea.jpg" alt="" srcset="">
            <div class="text-center fs-18 fw-500 q-mt-sm">Living Area</div>
          </div>
          <div class="col-4 image-container column items-center">
            <img src="~assets/bedroom.jpeg" alt="" srcset="">
            <div class="text-center fs-18 fw-500 q-mt-sm">Royal Bedroom</div>
          </div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2" class="column no-wrap" >
        <div class="row fit justify-start items-center q-gutter-md q-col-gutter no-wrap color-brown">
          <div class="col-4 image-container column items-center">
            <img src="~assets/livingarea.jpg" alt="" srcset="">
            <div class="text-center fs-18 fw-500 q-mt-sm">Living Area</div>
          </div>
          <div class="col-4 image-container column items-center">
            <img src="~assets/bedroom.jpeg" alt="" srcset="">
            <div class="text-center fs-18 fw-500 q-mt-sm">Royal Bedroom</div>
          </div>
        </div>
      </q-carousel-slide>
      </template>
      <template v-else>
      <q-carousel-slide :name="1" class="column no-wrap">
        <div class="image-container column items-center">
          <img src="~assets/kitchen.jpg" alt="" srcset="">
          <div class="text-center fs-18 fw-500 q-mt-sm">Kitchen Interiors</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="2" class="column no-wrap">
        <div class="image-container column items-center">
          <img src="~assets/livingarea.jpg" alt="" srcset="">
          <div class="text-center fs-18 fw-500 q-mt-sm">Living Area</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="3" class="column no-wrap">
        <div class="image-container column items-center">
          <img src="~assets/bedroom.jpeg" alt="" srcset="">
          <div class="text-center fs-18 fw-500 q-mt-sm">Royal Bedroom</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="4" class="column no-wrap">
        <div class="image-container column items-center">
          <img src="~assets/livingarea.jpg" alt="" srcset="">
          <div class="text-center fs-18 fw-500 q-mt-sm">Living Area</div>
        </div>
      </q-carousel-slide>
      <q-carousel-slide :name="5" class="column no-wrap">
        <div class="image-container column items-center">
          <img src="~assets/bedroom.jpeg" alt="" srcset="">
          <div class="text-center fs-18 fw-500 q-mt-sm">Royal Bedroom</div>
        </div>
      </q-carousel-slide>
      </template>
      <template v-slot:control>
        <q-carousel-control
          position="bottom-right"
          :offset="offset"
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
  </div>
</template>

<script>
import { ref } from 'vue'
export default {
  name: 'DesignServices',
  setup () {
      return {
        slide: ref(1),
        autoplay: ref(true)
      }
    },
  computed: {
    isDesktop () {
      return this.$q.screen.gt.sm
    },
    offset () {
      return this.isDesktop ? [10, 10] : [20, 50]
    }
  }
}
</script>

<style lang="scss" scoped>
.image-container {
  cursor: pointer;
  img {
    width: 80%;
  height: 400px;
  object-fit: cover;
  border-radius: 20px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
  @media only screen and (max-width: $breakpoint-sm-max) {
    width: 100%;
    height: 350px;
  }
  }
}

</style>
