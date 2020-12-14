<template>
  <div class="background">
    <v-container>
      <div class="text-center">
            <v-icon class="pt-10" size="50" color="#004e98"
              >mdi-email-outline
            </v-icon>

            <h1 class="font__main-alter">CONTACTO</h1>
            <v-card flat height="3" color="#004e98" width="300" class="mx-auto">
            </v-card>
            <h3 class="pt-1">Fuentes de contacto (Disponibilidad 24/7)</h3>
          </div>
      <v-row>
          <v-card-text class="text-center">
          <h2 class="h2 py-3">
            <v-icon size="23" class="pr-1" color="cyan">
              mdi-email-outline</v-icon
            >E-mail
          </h2>

          jesus.hdez@arcup.com.mx
           <h2 class="h2 py-3">
            <v-icon size="23" class="pr-1" color="cyan"> mdi-phone</v-icon
            >Teléfono
          </h2>
          
          (+52) 2281132016

          <h2 class="h2 py-3">
            <v-icon size="23" class="pr-1" color="cyan"> mdi-google-maps</v-icon
            >Ubicación
          </h2>
          
          Xalapa, Veracruz
        </v-card-text> 
      </v-row>
    </v-container>
  </div>
</template>
<style scoped>
.height {
  height: 80px;
}
.background {
  background-image: url("../assets/view-contact/image-1.png");
  background-size: cover;
}
</style>
