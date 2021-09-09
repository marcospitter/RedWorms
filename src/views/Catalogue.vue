<template>
  <div>
    <Products />
    <Seeds/>
  </div>
</template>

<script>

import Products from '../components/catalogue/Products.vue'
import Seeds from '../components/catalogue/Seeds.vue'

export default {
  components: { Products, Seeds },
}
</script>
