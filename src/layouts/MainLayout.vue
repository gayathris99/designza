<template>
  <q-layout view="lHh Lpr lFf">
    <designza-header/>
    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<script>
import DesignzaHeader from 'src/components/DesignzaHeader'
export default {
  name: 'MainLayout',
  components: { DesignzaHeader }
}
</script>
