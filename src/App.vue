<template>
  <div class="container">
    <HeaderItem @show-characters="getStarWarsCharacters()" />
    <GridItem :characters="characters" />
  </div>
</template>

<script>
import HeaderItem from "@/components/Header";
import GridItem from "@/components/Grid";

export default {
  name: 'App',
  components: {
    HeaderItem,
    GridItem
  },
  data() {
    return {
      characters: []
    }
  },
  methods: {
    async getStarWarsCharacters() {
      const res = await fetch('https://swapi.dev/api/people')
      const { results } = await res.json()
      this.characters = results
      //console.log(this.characters)
    },
  }
}
</script>

<style scoped>

</style>
