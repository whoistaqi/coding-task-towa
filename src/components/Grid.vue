<template>

  <div v-if="loading" class="d-flex justify-content-center align-items-center">
    <SpinnerItem />
    <SpinnerItem />
    <SpinnerItem />
  </div>

  <div v-else class="row">

    <div :key="character.name" v-for="character in characters" class="col-auto">
      <CardItem :character="character"/>
      <br>
    </div>

    <FooterItem
        :showPreviousButton="showPreviousButton"
        @show-previous-characters="$emit('show-previous-characters')"
        :showNextButton="showNextButton"
        @show-next-characters="$emit('show-next-characters')"
    />

  </div>

</template>

<script>
import SpinnerItem from "@/components/Spinner";
import CardItem from "@/components/Card";
import FooterItem from "@/components/Footer";

export default {
  name: 'GridItem',
  components: {
    SpinnerItem,
    CardItem,
    FooterItem,
  },
  props: {
    loading: Boolean,
    characters: Array,
    showPreviousButton: Boolean,
    showNextButton: Boolean
  },
  emits: ['show-previous-characters', 'show-next-characters']
}
</script>

<style scoped>
.d-flex {
  height: 80vh;
}
</style>