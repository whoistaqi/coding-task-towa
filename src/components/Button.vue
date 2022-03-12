<template>
  <button @click="getStarWarsCharacters()" class="btn btn-success">Show Characters</button>
</template>

<script>
export default {
  name: 'ButtonItem',
  methods: {
    async getStarWarsCharacters() {

      const res = await fetch('https://swapi.dev/api/people')
      const { results } = await res.json()

      console.log(results)
    }
  }
}
</script>