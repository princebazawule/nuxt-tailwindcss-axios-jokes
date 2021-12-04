<template>
  <div class="flex flex-col justify-center items-center min-h-screen">
    <h1 class="text-6xl font-bold p-8">Welcome to jokes!</h1>
    <p class="text-3xl">Hope you're ready to laugh...</p>
  </div>
</template>

<script>
export default {
    head() {
        return {
          title: 'Nuxt Jokes | Home',
          meta: [
              {
                  hid: 'description',
                  name: 'description',
                  content: 'A simple joke generation app'
              }
          ],
        }
    }
}
</script>
