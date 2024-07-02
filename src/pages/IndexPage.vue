<template>
  <q-page class="font-mona">
    <hero-banner/>
    <success-stories/>
    <the-process/>
  </q-page>
</template>

<script>
import HeroBanner from 'src/components/HeroBanner'
import SuccessStories from 'src/components/SuccessStories'
import TheProcess from 'src/components/TheProcess'
export default {
  name: 'IndexPage',
  components: { HeroBanner, SuccessStories, TheProcess }
}
</script>
