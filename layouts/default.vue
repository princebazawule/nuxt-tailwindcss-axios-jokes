<template>
  <div class='min-h-screen'>
      <TheHeader />
      <Nuxt />
      <TheFooter />
  </div>
</template>

<script>
import TheFooter from '../components/TheFooter.vue'
import TheHeader from '../components/TheHeader.vue'

export default {
  components: { TheHeader, TheFooter },
  // head() {
  //     return {
  //       meta: [
  //           { charset: 'utf-8' },
  //           { name: 'viewport', content: 'width=device-width, initial-scale=1' },
  //       ],
  //       link: [{ rel: 'icon', type: 'image/x-icon', href: '/favicon.ico' }]
  //     }
  // }

}
</script>

<style>

</style>