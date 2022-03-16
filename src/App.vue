<template>
  <div class="container">
    <HeaderItem :showStarWarsCharacters="showStarWarsCharacters" @toggle-grid="toggleShowCharacters()" />
    <GridItem
        v-show="showStarWarsCharacters"
        :loading="loading"
        :characters="characters"
        :showPreviousButton="showPreviousButton"
        @show-previous-characters="showPreviousCharacters()"
        :showNextButton="showNextButton"
        @show-next-characters="showNextCharacters()"
    />
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
      loading: false,
      characters: [],
      showStarWarsCharacters: false,
      page: 1,
      showNextButton: true,
      showPreviousButton: true,
    }
  },
  methods: {
    toggleShowCharacters() {
      this.showStarWarsCharacters = !this.showStarWarsCharacters
    },
    async getStarWarsCharacters() {
      this.loading = true
      this.showPreviousButton = this.page !== 1;
      try {
        const res = await fetch('https://swapi.dev/api/people/?page='+this.page)
        const data = await res.json()
        this.loading = false
        this.showNextButton = data.next !== null;
        return data.results
      } catch (error) {
        console.log(error)
        this.loading = false
      }
    },
    async showNextCharacters() {
      this.page++
      this.characters = await this.getStarWarsCharacters()
    },
    async showPreviousCharacters() {
      this.page--
      this.characters = await this.getStarWarsCharacters()
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
