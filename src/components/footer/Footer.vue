<template>
  <v-footer
    color="grey lighten-2"
    padless
    dark
  >
    <v-row
      justify="center"
      no-gutters
    >
      <v-btn
        v-for="link in links"
        :key="link.title"
        :to="link.route"
        text
        class="my-2 grey--text"
      >
        {{ link.title }}
      </v-btn>
      <v-col
        class="grey lighten-1 py-4 text-center grey--text"
        cols="12"
      >
        {{ new Date().getFullYear() }} — <strong>RedWorms</strong>
      </v-col>
    </v-row>
  </v-footer>
</template>

<script>

  
  export default {
    data: () => {
    return {
      links: [
        { icon: 'mdi-home', title: 'Volver al inicio', route: '/' },
        { icon: 'mdi-store', title: 'Catálogo', route: '/catalogue' },
        { icon: 'mdi-email', title: 'Contacto', route: '/contact' }
      ]
    }
  }
  }
</script>