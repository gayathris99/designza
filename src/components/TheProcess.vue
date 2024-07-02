<template>
  <div class="q-my-xl color-brown font-mona">
    <div class="text-center fs-36 q-mb-md">
      <span class="fw-900">CUSTOMER SATISFACTION &</span> <span class="fw-600"> <br/> THE PROCESS BEHIND</span>
    </div>
    <div class="row items-center justify-start q-px-xl" :class="isDesktop ? 'q-mx-xl' : ''">
      <div class="col-md-6 col-sm-12 col-xs-12">
        <!-- Steps -->
        <div class="step-container row items-center q-gutter-x-lg align-center q-mt-lg">
          <img src="~assets/stepimage.jpg" alt="">
          <div class="step-title fs-18">
            <span class="color-grey fw-500">01 &nbsp;</span>
            <span class="fw-600">INSPECTION AND <br/>CLIENT CONSULTATION</span>
          </div>
        </div>
        <div class="border-class"></div>
        <!-- Steps -->
        <div class="step-container row items-center q-gutter-x-lg align-center q-mt-lg">
          <img src="~assets/stepimage2.jpg" alt="">
          <div class="step-title fs-18">
            <span class="color-grey fw-500">02 &nbsp;</span>
            <span class="fw-600">CONCEPT AND <br/>DESIGN DEVELOPMENT</span>
          </div>
        </div>
        <div class="border-class"></div>
        <!-- Steps -->
        <div class="step-container row items-center q-gutter-x-lg align-center q-mt-lg">
          <img src="~assets/stepimage3.jpg" alt="">
          <div class="step-title fs-18">
            <span class="color-grey fw-500">03 &nbsp;</span>
            <span class="fw-600">CONSTRUCTION AND <br/>INSTALLATION</span>
          </div>
        </div>
        <div class="border-class"></div>
        <!-- Steps -->
        <div class="step-container row items-center q-gutter-x-lg align-center q-mt-lg">
          <img src="~assets/stepimage4.jpeg" alt="">
          <div class="step-title fs-18">
            <span class="color-grey fw-500">04 &nbsp;</span>
            <span class="fw-600">WALKTHROUGH, APPROVAL <br v-if="isDesktop"/>AND HANDOVER</span>
          </div>
        </div>
      </div>
      <div class="col-md-6 col-sm-12 col-xs-12 right-side-container">
        <img src="~assets/mainstepimage.jpeg" alt="">
        <div class="q-mt-md">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Incidunt a porro corporis doloremque, delectus minima eius optio expedita maxime ad ex repellendus sunt dolor distinctio odit. Quo sit sed blanditiis!</div>
        <div class="flex flex-center">
          <q-btn class="q-mt-sm color-white background-brown fw-700" size="25" rounded label="GET A QUOTE" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'TheProcess',
  computed: {
    isDesktop () {
      return this.$q.screen.gt.sm
    }
  }
}
</script>

<style lang="scss" scoped>
.step-container {
  img {
    width: auto;
    max-height: 100px;
    object-fit: cover;
    border-radius: 20px;
    box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2), 0 6px 20px 0 rgba(0, 0, 0, 0.19);
    @media only screen and (max-width: $breakpoint-sm-max) {
      width: 100%;
      max-height: 125px;
      margin-bottom: 20px;
    }
  }
}
.right-side-container {
  img {
    border-radius: 20px;
    max-height: 400px;
    width: auto;
    object-fit: cover;
    @media only screen and (max-width: $breakpoint-sm-max) {
      width: 100%;
      max-height: 200px;
      margin-top: 40px;
    }
  }
}
.border-class {
  width: 75%;
  margin-top: 16px;
  border-bottom: 1px solid #E5E4E2;
  @media only screen and (max-width: $breakpoint-sm-max) {
    width: 100%
  }
}
</style>
