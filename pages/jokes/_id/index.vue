<template>
  <div class="flex flex-col justify-center items-center min-h-screen">
    <NuxtLink to="/jokes">Back to Jokes</NuxtLink>

    <h1 class="text-3xl font-bold py-8 px-8 border-t-2 border-b-4 my-4 text-center" v-if="joke">
        {{ joke }}
    </h1>
    
    <div>{{ $route.params.id }}</div>
  </div>
</template>

<script>
import axios from "axios"

export default {
    data() {
        return {
            joke: {}
        }
    },
    async created() {
        const config = {
            headers: {
                'Accept': 'application/json'
            }
        }

        try {
            const res = await axios.get(`https://icanhazdadjoke.com/j/${this.$route.params.id}`, config)
            console.log(res.data)
            this.joke = res.data.joke
        } catch (error) {
            console.log(error)
        }
        
    },
    head() {
        return {
            title: this.joke,
            meta: [
                {
                    hid: 'description',
                    name: 'description',
                    content: this.joke
                }
            ],
        }
    }
}
</script>

<style></style>
