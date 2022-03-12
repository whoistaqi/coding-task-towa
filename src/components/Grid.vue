<template>

  <div class="row">

    <div :key="i" v-for="i in 9" class="col">
      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character {{i}}
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>
      <br>
    </div>

    <!--
    <div class="col">

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

    </div>
    <div class="col">

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

    </div>
    <div class="col">

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

      <div class="card" style="width: 18rem;">
        <div class="card-header">
          Character 1
        </div>
        <ul class="list-group list-group-flush">
          <li class="list-group-item"><strong>Gender:</strong> {people.gender}</li>
          <li class="list-group-item"><strong>Height:</strong> {people.height}</li>
          <li class="list-group-item"><strong>Eye Color:</strong> {people.eye_color}</li>
        </ul>
      </div>

      <br>

    </div>

    -->
  </div>

</template>

<script>
export default {
  name: 'GridItem',
}
</script>