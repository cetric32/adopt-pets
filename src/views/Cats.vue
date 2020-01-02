<template>
  <div>
    <h1>Cats for Adoption</h1>
    <table class="table table-striped table-dark table-hover">
      <thead>
        <tr>
          <th scope="col">#</th>
          <th scope="col">Name</th>
          <th scope="col">Breed</th>
          <th scope="col">Gender</th>
          <th scope="col">Age</th>
          <th scope="col">Color</th>
          <th scope="col">Weight</th>
          <th scope="col">Location</th>
          <th scope="col">Notes</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(cat,index) in cats" :key="index">
          <th scope="row">{{index}}</th>
          <td>
            <router-link :to="`/pets/cats/${index}`"> {{cat.name}}</router-link>
          </td>
          <td>{{cat.breed}}</td>
          <td>{{cat.gender}}</td>
          <td>{{cat.age}}</td>
          <td>{{cat.color}}</td>
          <td>{{cat.weight}}</td>
          <td>{{cat.location}}</td>
          <td>{{cat.notes}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'Cats',
  data () {
    return {}
  },
  computed: {
    ...mapState([
      'cats'
    ])
  }
}
</script>

<style>

</style>
