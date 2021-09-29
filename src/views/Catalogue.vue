<template>
  <div>
    <Products/>
    <Seeds/>
  </div>
</template>

<script>

import Products from '../components/catalogue/products/Products.vue'
import Seeds from '../components/catalogue/seeds/Seeds.vue'

export default {
  components: { Products, Seeds },
}
</script>
