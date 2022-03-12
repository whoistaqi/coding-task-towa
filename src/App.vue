<template>
  <div class="container">
    <HeaderItem />
    <GridItem />
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
  }
}
</script>

<style scoped>

</style>
