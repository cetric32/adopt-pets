<template>
  <div>
    <h1>Dogs for Adoption</h1>
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
          <th scope="col">Lodogion</th>
          <th scope="col">Notes</th>
        </tr>
      </thead>
      <tbody>
        <tr v-for="(dog,index) in dogs" :key="index">
          <th scope="row">{{index}}</th>
          <td>
            <router-link :to="`/pets/dogs/${index}`"> {{dog.name}}</router-link>
          </td>
          <td>{{dog.breed}}</td>
          <td>{{dog.gender}}</td>
          <td>{{dog.age}}</td>
          <td>{{dog.color}}</td>
          <td>{{dog.weight}}</td>
          <td>{{dog.lodogion}}</td>
          <td>{{dog.notes}}</td>
        </tr>
      </tbody>
    </table>
  </div>
</template>

<script>
import { mapState } from 'vuex'

export default {
  name: 'Dogs',
  data () {
    return {}
  },
  computed: {
    ...mapState([
      'dogs'
    ])
  }
}
</script>

<style>

</style>
