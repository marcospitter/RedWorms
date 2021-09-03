<template>
  <v-app>
    <Navbar />
    <v-main class="grey lighten-5">
      <router-view></router-view>
    </v-main>
  </v-app>
</template>

<script>
import Navbar from '@/components/navbar/Navbar'

export default {
  name: 'App',
  components: { Navbar },
  data () {
    return {
    //
    }
  }
}
</script>
