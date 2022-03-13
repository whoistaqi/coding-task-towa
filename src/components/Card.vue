<template>
  <div class="card" style="width: 18rem;">
    <div class="card-header">

      <strong> {{ character.name }} </strong>
    </div>
    <ul class="list-group list-group-flush">
      <li class="list-group-item"><strong>Gender:</strong> {{ character.gender }}</li>
      <li class="list-group-item"><strong>Height:</strong> {{ character.height }} cm</li>
      <li class="list-group-item"><strong>Eye Color:</strong> {{ character.eye_color }}</li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'CardItem',
  props: {
    character: Object,
  },
}
</script>

<style scoped>
.card {
  border-radius: 20px;
  border-color: black;
}
.card-header {
  border-radius: 20px 20px 0 0;
  padding-top: 16px;
  padding-bottom: 8px;
}
.list-group-item {
  background: none;
}
</style>