<template>
  <div class="container">
    <HeaderItem :showStarWarsCharacters="showStarWarsCharacters" @toggle-grid="toggleShowCharacters()" />
    <GridItem
        v-show="showStarWarsCharacters"
        :characters="characters"
        :showPreviousButton="showPreviousButton"
        @show-previous-characters="showPreviousCharacters()"
        :showNextButton="showNextButton"
        @show-next-characters="showNextCharacters()"
    />
    <footer>
<!--      <button v-show="showPreviousButton" @click="showPreviousCharacters()" class="btn btn-light">previous</button>-->
<!--      <button v-show="showNextButton" @click="showNextCharacters()" class="btn btn-light">next</button>-->
    </footer>
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
      showStarWarsCharacters: false,
      page: 1,  //new
      showNextButton: true,
      showPreviousButton: true,
    }
  },
  methods: {
    toggleShowCharacters() {
      this.showStarWarsCharacters = !this.showStarWarsCharacters
    },
    async getStarWarsCharacters() {
      console.log(this.page)
      this.showPreviousButton = this.page !== 1;
      const res = await fetch('https://swapi.dev/api/people/?page='+this.page)
      const data = await res.json()
      this.showNextButton = data.next !== null;
      return data.results
      //console.log(this.characters)
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
