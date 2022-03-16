<template>
  <footer>

    <div class="d-flex flex-row-reverse">
      <div class="p-2">
        <ButtonItem
            v-show="showNextButton"
            @btn-click="$emit('show-next-characters')"
            :text="'>>'"
            :classText="'btn btn-light'"
        />
      </div>

      <div class="p-2">
        <ButtonItem
            v-show="showPreviousButton"
            @btn-click="$emit('show-previous-characters')"
            :text="'<<'"
            :classText="'btn btn-light'"
        />
      </div>
    </div>

  </footer>
</template>

<script>
import ButtonItem from "@/components/Button";

export default {
  name: "FooterItem",
  components: {
    ButtonItem
  },
  props: {
    showPreviousButton: Boolean,
    showNextButton: Boolean,
  },
  emits: ['show-previous-characters', 'show-next-characters'],
}
</script>

<style scoped>

</style>