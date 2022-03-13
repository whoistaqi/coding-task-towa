<template>
  <div class="container">
    <HeaderItem :showStarWarsCharacters="showStarWarsCharacters" @toggle-grid="toggleShowCharacters()" />
    <GridItem v-show="showStarWarsCharacters" :characters="characters" />
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
      characters: [],
      showStarWarsCharacters: false
    }
  },
  methods: {
    toggleShowCharacters() {
      this.showStarWarsCharacters = !this.showStarWarsCharacters
    },
    async getStarWarsCharacters() {
      const res = await fetch('https://swapi.dev/api/people')
      const { results } = await res.json()
      return results
      //console.log(this.characters)
    }
  },
  async created() {
    this.characters = await this.getStarWarsCharacters()
  }
}
</script>

<style scoped>
.container {
  margin-top: 20px;
}

</style>
