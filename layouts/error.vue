<template>
  <div class="flex flex-col justify-center items-center min-h-screen">
    <h1 v-if="error.statusCode === 404" class="text-6xl font-bold p-8">404 | Page not found</h1>
    <h1 v-else class="text-6xl font-bold p-8">An error occurred</h1>

    <NuxtLink to="/" class="text-3xl">Go to the Home page</NuxtLink>
  </div>
</template>

<script>
  export default {
    props: ['error'],
    layout: 'error' // you can set a custom layout for the error page
  }
</script>