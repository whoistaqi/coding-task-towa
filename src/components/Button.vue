<template>
  <button @click="$emit('show-characters')" class="btn btn-success">Show Characters</button>
</template>

<script>
export default {
  name: 'ButtonItem',
  emits: ['show-characters']
}
</script>

<style scoped>
button {
  margin-left: 20px;
}
</style>