<template>
  <NuxtLink :to="'jokes/'+id">
      <div class="joke">
        <p>{{ joke.joke }}</p>
    </div>
  </NuxtLink>
</template>

<script>
export default {
    name: 'Joke',
    props: ['joke', 'id']
}
</script>