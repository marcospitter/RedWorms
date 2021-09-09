<template>
  <v-app>
    <Navbar />
    <v-main class="grey lighten-5">
      <router-view></router-view>
    </v-main>
    <Footer />
  </v-app>
</template>

<script>
import Navbar from '@/components/navbar/Navbar'
import Footer from '@/components/footer/Footer'

export default {
  name: 'App',
  components: { Navbar, Footer },
  data () {
    return {
    //
    }
  }
}
</script>
