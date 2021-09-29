<template>
  <v-container
    my-5>
    <h2>Catálogo de Semillas</h2>
    <v-card
      flat
      class="pa-3">
      <p>
        Tenemos una gran cantidad de <span>semillas en stock</span> para que siembres durante todo el año. Enterate mucho más sobre el <span>calendario de siembra</span> en nuestro perfil de Instagram.
      </p>
    </v-card>
    
    
    <v-expansion-panels>
     
      <v-expansion-panel
        :disabled="product.disable"
        v-for="product in seeds"
        :key="product.title"
        class="px-0">

        <v-expansion-panel-header>
          {{ product.title }}
          <v-spacer></v-spacer>
          <strong
            v-if="product.disable == true">
            (SIN STOCK)
          </strong>
          
        </v-expansion-panel-header>
    
        <v-expansion-panel-content>
          

            <v-row>  
            
              <v-col cols="12" sm="4"
                align-self="center"
                class="justify-center">  
                <v-img
                  :src='product.image.url'
                  alt="producto"
                  min-height="70"
                  min-width="70"
                  max-height="200"
                  max-width="200"
                  
                  contain
                  class="mx-auto">
                </v-img>
              </v-col>
            
              <v-col 
                align-self="center" 
                class="text-center">
                
                <h5>
                  {{ product.subtitle }}
                </h5>
                <p>
                  {{ product.description }}
                </p>
              </v-col>
            </v-row>
          
        </v-expansion-panel-content>
      </v-expansion-panel>
    </v-expansion-panels>
  </v-container>
  
</template>

<style scoped>
  span {
    font-weight: bold;
  }
</style>

<script defer src="./seeds.js"></script>
