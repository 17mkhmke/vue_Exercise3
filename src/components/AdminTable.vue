<template>
  <div class="container">
    <div class="row">
      <h1 class="display-1"> Admin</h1>
    </div>
    <table class="table table-striped">
    <tr>
      <th>Name</th>
      <th>Description</th>
      <th>Price</th>
      <th>Image</th>
      <th>Actions</th>
    </tr>
    <tr v-for="products in products" :key="products">
      <td>{{ products.make }}</td>
      <td>{{ products.spec }}</td>
      <td>R{{ products.amount }}</td>
      <td><img :src= "products.image" :class="prdImage"> </td>
      <td> <button type="button" class="btn btn-success">Edit</button>
  <button type="button" class="btn btn-danger">Delete</button> </td>
    </tr>
  </table>
  </div>
</template>
<script>
import { mapActions, mapGetters } from 'vuex'
export default {
  name: 'AdminTable',
  computed: {
    ...mapGetters(['products'])
  },
  methods: {
    ...mapActions(['fetchAllProducts'])
  },
  created () {
    this.fetchAllProducts()
  }
}
</script>
