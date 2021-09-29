<template>
  <v-container
    class="my-5">
    <h2 class="d-block py-5">
      Todos los productos y semillas de nuestra tienda los encontrás acá.
    </h2>
    <v-card
      flat
      class="pa-3">
      <p>
        Los productos que ofrece RedWorms son <span>100% orgánicos y ecológicos</span> o construidos con material <span>reciclable o reutilizado</span>. Tenemos composteras, cajones huerteros artesanales, insecticidas orgánicos y mucho más. 
      </p>
    </v-card>
    
    
    <v-row
      class="py-5"
      justify="center"
      align="center">
    
      <v-col
        cols="12" sm="6" lg="4"
        v-for=" product in products " 
        :key="product.title">
        
        <v-card
          :disabled="product.disable"
          class="ma-auto"
          max-width="450">
            
          <v-img
            :src='product.image.url'
            alt="producto">
          </v-img>

            <v-card-title>
              {{ product.title }}
            </v-card-title>

            <v-card-subtitle>
              {{ product.subtitle }}
            </v-card-subtitle>

            <v-card-actions>
              <v-btn
                  @click="product.showDescription = !product.showDescription"
                  color="grey"
                  text
                  class="mx-auto"
                  exact-active-class>{{ product.disable ? 'SIN STOCK' : 'mas' }}
                    
                    <v-icon>{{ product.showDescription ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
              </v-btn>
            </v-card-actions>

            <v-expand-transition>
              <div v-show="product.showDescription">
                
                <v-divider></v-divider>

                <v-card-text>
                {{ product.description }}
                </v-card-text>
              </div>
            </v-expand-transition>

        </v-card>
      </v-col> 
    </v-row>
  </v-container>
</template>

<style scoped>
  span {
    font-weight: bold;
  }
</style>

<script defer src="./products.js"></script>
