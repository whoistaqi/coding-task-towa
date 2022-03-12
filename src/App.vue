<template>
  <div class="container">
    <HeaderItem />
    <div class="row">
      <div class="col">
        Column
      </div>
      <div class="col">
        Column
      </div>
      <div class="col">
        Column
      </div>
    </div>
  </div>
</template>

<script>
import HeaderItem from "@/components/Header";

export default {
  name: 'App',
  components: {
    HeaderItem,
  }
}
</script>

<style scoped>

</style>
