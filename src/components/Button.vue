<template>
  <button @click="$emit('btn-click')" :class="classText" >{{ text }}</button>
</template>

<script>
export default {
  name: 'ButtonItem',
  props: {
    text: String,
    classText: String
  },
  emits: ['btn-click']
}
</script>

<style scoped>
button {
  margin-left: 20px;
}
.btn-light {
  color: white;
  background-color: transparent;
  border-color: #f8f9fa;
  font-weight: bold;
}
.btn-light:hover {
  color: black;
  background-color: white;
}
</style>