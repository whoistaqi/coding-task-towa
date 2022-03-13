<template>
  <header>
    <h1>Star Wars Characters</h1>
    <ButtonItem @show-characters="$emit('show-characters')"/>
  </header>
</template>

<script>
import ButtonItem from "@/components/Button";

export default {
  name: 'HeaderItem',
  components: {
    ButtonItem
  },
  emits: ['show-characters']
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 20px;
}
</style>