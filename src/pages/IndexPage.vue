<template>
  <q-page class="font-mona">
    <hero-banner/>
    <success-stories/>
    <the-process/>
    <projectin-mind/>
    <client-reviews/>
  </q-page>
</template>

<script>
import HeroBanner from 'src/components/HeroBanner'
import SuccessStories from 'src/components/SuccessStories'
import TheProcess from 'src/components/TheProcess'
import ProjectinMind from 'src/components/ProjectinMind'
import ClientReviews from 'src/components/ClientReviews'
export default {
  name: 'IndexPage',
  components: { HeroBanner, SuccessStories, TheProcess, ProjectinMind, ClientReviews }
}
</script>

    ClientReviews
