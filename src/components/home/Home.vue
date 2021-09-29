<template>
  <div>
    <div
      height="100px">  
      <v-img 
        class="mx-auto mt-3"
        max-width="200px" 
        position="center" 
        src="@/assets/logos/logo.png">
      </v-img>
    </div>
        
    <v-container>
      <h1>Bienvenidos a nuestro sitio web!</h1>
      <h3
        class="my-2">
        ¿Quiénes somos?
      </h3>
      <v-row>
        <v-col
          cols="12" sm="6"
          class="display-flex mr-auto my-2">
          <div
            class="mx-auto my-2">
            <p
              class="my-2">
              RedWorms es un <span>emprendimiento independiente</span> que ofrece productos ecológicos e ideas novedosas sobre <span>huerta y compostaje</span>. ¡Tenemos todo lo necesario para que empieces!</p>
          </div>
        </v-col>
      </v-row>
      
      <v-responsive>
        <v-carousel 
          fluid
          class="mt-3"
          cycle
          hide-delimiters
          height="200">
          <v-carousel-item
            v-for="(item,i) in items"
            :key="i"
            :src="item.src">
          </v-carousel-item>
        </v-carousel>
      </v-responsive>
      
      <v-col
        class="mx-auto"
        cols="12"
        sm="8">
        <p>Nuestro objetivo es el de llevar concientización y generar hábitos sustentables en el manejo de nuestros desechos. La propuesta de RedWorms es incentivar las buenas prácticas desde el lugar en el que estemos, mediante procedimientos que no generan trabajo, no toman tiempo ni complicación alguna.</p>    
        <h3>Pero, ¿por qué el compostaje?</h3>
        <p>Porque compostar no sólo cuida el planeta; También es una manera mucho mas cómoda y limpia de tratar estos desechos. El compostaje reduce notablemente tu cantidad de basura diaria, no contamina, no despide olor, no ocupa lugar, reduce su volumen a través de un proceso natural de descomposición, y a cambio te da un abono natural para tu jardín, huerta, o para quedar bien con alguien que lo utilice. ¡Cierra por todos lados!</p>
        <p>Entre los productos destacados de nuestro catálogo podés encontrar lombrices californianas, composteras, tierra fertilizada, semillas para tu huerta, cajones huerteros y mucho más.</p>
        <p>No se trata de que cambies tu vida en favor de la ecología. Se trata, dentro de lo que no nos cuesta nada hacer, de dejar una huella un poquito mas pequeña en nuestro paso por el medioambiente.</p>
      </v-col>
      <v-card
          class="my-3 mx-auto"
          color="#26c6da"
          dark
          max-width="400">
          <v-card-text 
            class="text-h5 font-weight-bold">
            El compostaje es la manera más efectiva de reducir el volumen de basura que sacamos a la calle. separar tus residuos orgánicos de los Inorgánicos también generará un máximo aprovechamiento de los materiales reciclables que descartamos. recordá: juntos son basura, pero separados son recursos.
          </v-card-text>
      </v-card>
    </v-container>

  </div>
</template>

<style src="./home.css"></style> 
<script src="./home.js"></script>