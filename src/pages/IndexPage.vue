<template>
  <q-page class="font-mona">
    <!-- <hero-banner/> -->
    <design-services/>
    <success-stories/>
    <the-process/>
    <projectin-mind/>
    <client-reviews/>
  </q-page>
</template>

<script>
// import HeroBanner from 'src/components/HeroBanner'
import SuccessStories from 'src/components/SuccessStories'
import TheProcess from 'src/components/TheProcess'
import ProjectinMind from 'src/components/ProjectinMind'
import ClientReviews from 'src/components/ClientReviews'
import DesignServices from 'src/components/DesignServices'
export default {
  name: 'IndexPage',
  components: { SuccessStories, TheProcess, ProjectinMind, ClientReviews, DesignServices }
  // components: { HeroBanner, SuccessStories, TheProcess, ProjectinMind, ClientReviews, DesignServices }
}
</script>

    ClientReviews
