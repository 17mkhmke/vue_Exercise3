<template>
  <div class="container">
    <div class="row">
      <h1 class="display-1"> Products</h1>
    </div>
    <div v-for="product in products" :key="product">>
        <div class="card-group" style="width: 18rem;">
            <img :src="product.image" class="card-img-top picture" alt="productImage">
            <div class="card-body">
                <h3 class="card-title">{{product.make}}</h3>
                <p class="card-text">{{product.spec}}</p>
                <label class="card-label">R{{product.amount}}</label><br>
                <button class="btn">Add To Cart</button>
            </div>
        </div>
    </div>
  </div>
</template>
<script>
import { mapActions, mapGetters } from 'vuex'
export default {
  name: 'productsComponent',
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
