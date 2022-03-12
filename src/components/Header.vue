<template>
  <header>
    <h1>Star Wars Characters</h1>
    <ButtonItem />
  </header>
</template>

<script>
import ButtonItem from "@/components/Button";

export default {
  name: 'HeaderItem',
  components: {
    ButtonItem
  }
}
</script>

<style scoped>
header {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 20px;
}
</style>