<template>

  <div class="row">

    <div :key="character.mass" v-for="character in characters" class="col-auto">
      <CardItem :character="character"/>
      <br>
    </div>

  </div>

</template>

<script>
import CardItem from "@/components/Card";

export default {
  name: 'GridItem',
  components: {
    CardItem
  },
  props: {
    characters: Array,
  },
}
</script>