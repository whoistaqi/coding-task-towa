<template>
  <header>
    <h1>Star Wars Characters</h1>
    <ButtonItem
        @btn-click="$emit('toggle-grid')"
        :text="showStarWarsCharacters ? 'Hide Characters' : 'Show Characters'"
        :classText="showStarWarsCharacters ? 'btn btn-danger' : 'btn btn-success'"
    />
  </header>
</template>

<script>
import ButtonItem from "@/components/Button";

export default {
  name: 'HeaderItem',
  components: {
    ButtonItem
  },
  props: {
    showStarWarsCharacters: Boolean
  },
  emits: ['toggle-grid']
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
h1 {
  color: white;
}
</style>