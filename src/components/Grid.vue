<template>

  <div class="row">

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
import CardItem from "@/components/Card";
import FooterItem from "@/components/Footer";

export default {
  name: 'GridItem',
  components: {
    CardItem,
    FooterItem
  },
  props: {
    characters: Array,
    showPreviousButton: Boolean,
    showNextButton: Boolean
  },
  emits: ['show-previous-characters', 'show-next-characters']
}
</script>