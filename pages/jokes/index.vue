<template>
    <div>
        <h1>List of Jokes</h1>
        <SearchJokes v-on:search-text="searchText" />
        <Joke 
            v-for="joke in jokes" 
            :key="joke.id" 
            :id="joke.id" 
            :joke="joke" />
    </div>
</template>

<script>
import axios from "axios";
import Joke from '../../components/Joke.vue';
import SearchJokes from '../../components/SearchJokes.vue';

export default {
  components: { Joke, SearchJokes },
    data() {
        return {
            jokes: []
        }
    },
    async created() {
        const config = {
            headers: {
                'Accept': 'application/json'
            }
        }

        try {
            const res = await axios.get('https://icanhazdadjoke.com/search', config)
            // console.log(res.data)
            this.jokes = res.data.results
        } catch (error) {
            console.log(error)
        }
        
    },
    methods: {
        async searchText(text) {
            const config = {
                headers: {
                    'Accept': 'application/json'
                }
            }

            try {
                const res = await axios.get(`https://icanhazdadjoke.com/search?term=${text}`, config)

                this.jokes = res.data.results
            } catch (error) {
                console.log(error)
            }
             
        }
    },
    head: {
        title: 'Nuxt Jokes | Joke Listings',
        meta: [
            {
                hid: 'description',
                name: 'description',
                content: 'List of Jokes'
            }
        ],
    }
}
</script>

<style>

</style>