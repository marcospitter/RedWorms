<template>
  <v-card>
    <v-app-bar
      app 
      flat 
      dark
      shrink-on-scroll
      fade-img-on-scroll
      src="https://cdn.pixabay.com/photo/2015/03/26/10/38/greenhouse-691704_960_720.jpg">
      
      <!--background image-->
      <template 
        v-slot:img="{ props }">
        <v-img
          dark
          v-bind="props">
        </v-img>
      </template>
      
      <v-app-bar-nav-icon
        @click="drawer = !drawer">
      </v-app-bar-nav-icon>
      
      <v-toolbar-title>
        RedWorms
      </v-toolbar-title>
      
      <template 
        v-slot:extension>  
        <v-tabs
          dark
          centered
          light>
          
          <v-tab 
            v-for="link in links"
            :key="link.title" 
            router :to="link.route">
            {{ link.title }}
          </v-tab>
          
        </v-tabs>
      </template>
    </v-app-bar>

    <!--Left navigation drawer-->
    <v-navigation-drawer 
      app 
      temporary 
      v-model="drawer">

      <v-list-item>
        <v-list-item-content>
          <v-list-item-title 
            class="text-h6">
            RedWorms
          </v-list-item-title>
          <v-list-item-subtitle>
            <v-icon>mdi-map-marker</v-icon>
            <a class="ubication"
              href="https://www.google.com/search?q=herrera+entre+rios+maps&sxsrf=ALeKk02cNCGDjSYBZgOlYDSJMaCPKdAkxw%3A1628804940211&ei=TJcVYZChDPrR1sQP6ral4A4&oq=herrera+entre+rios+maps&gs_lcp=Cgxnd3Mtd2l6LXNlcnAQAzICCCYyAggmMgYIABANEB4yAggmMgIIJjICCCY6BwgAEEcQsAM6BggAEBYQHjoJCAAQFhAeEIsDSgQIQRgAUIRJWKpYYPVcaAFwAngAgAFxiAHlBJIBAzIuNJgBAKABAcgBCLgBAsABAQ&sclient=gws-wiz-serp&ved=0ahUKEwiQ9_meu6zyAhX6qJUCHWpbCewQ4dUDCA4&uact=5#">
              Herrera, ER
            </a>
          </v-list-item-subtitle>
        </v-list-item-content>
      </v-list-item>

      <v-divider></v-divider>
        <!--menus-->
        <v-list>
          <v-list-item
            v-for="link in links" 
            :key="link.title" 
            router 
            :to="link.route">
            <v-list-item-action>
              <v-icon>{{ link.icon }}</v-icon>
            </v-list-item-action>
            <v-list-item-content>
              <v-list-item-title>{{ link.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>  
          <v-divider></v-divider>
          <v-list-item>
            <v-list-item-subtitle>
              <a
                href="https://www.redcompostaje.org.ar/">
                Página de Red de Compostaje
              </a>
            </v-list-item-subtitle>
          </v-list-item>
        </v-list>
    </v-navigation-drawer>
  </v-card>

</template>

<style scoped>

a {
  color: inherit !important;
}
a.ubication {
  text-decoration: none; 
}
</style>

<script>
export default {
  name: 'Navbar',
  data: () => {
    return {
      drawer: false,
      links: [
        { icon: 'mdi-home', title: 'Inicio', route: '/' },
        { icon: 'mdi-store', title: 'Catálogo', route: '/catalogue' },
        { icon: 'mdi-email', title: 'Contacto', route: '/contact' }
      ]
    }
  }
}
</script>