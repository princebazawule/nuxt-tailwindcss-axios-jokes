<template>
  <div class="flex flex-col justify-center items-center min-h-screen">
    <h1 class="text-6xl font-bold p-8">About jokes</h1>
    <p class="text-3xl">A simple joke generation app...</p>
  </div>
</template>

<script>
export default {
    head() {
        return {
          title: 'Nuxt Jokes | About',
          meta: [
              {
                  hid: 'description',
                  name: 'description',
                  content: 'About the jokes generation app'
              }
          ],
        }
    }
}
</script>

<style>

</style>