<template>
  <div>
    <v-row>
      <v-col class="pa-0 ma-0" cols="12" sm="6" md="6" lg="6" xl="6">
        <v-card
          class="pa-10 d-flex align-content-center flex-wrap"
          color="#EBEBEB"
          rounded="0"
          flat
          height="100%"
        >
          <h1 class="color-blue pl-2 font-tile">
            Ingeniero De Software
            <v-icon class="pl-1" size="34" color="#FF6700"
              >mdi-laptop-chromebook</v-icon
            >
          </h1>
          <h1 class="font-size-title font-tile">JESÚS HERNÁNDEZ</h1>

          <h3>
            Planificamos una reunión entre el cliente y el equipo de trabajo
            para obtener las características, funcionalidades y reglas del
            negocio que se implementarán en el sistema de software.
          </h3>
        </v-card>
      </v-col>
      <v-col class="" cols="12" sm="6" md="6" lg="6" xl="6">
        <v-card
          class="text-center d-flex align-content-center flex-wrap"
          color="#EBEBEB"
          rounded="0"
          flat
          height="100%"
        >
          <v-img
            max-width="100%"
            max-height="100%"
            src="../assets/view-home/image-1.png"
          >
          </v-img>
        </v-card>
      </v-col>
    </v-row>
  </div>
</template>
<style scoped>
@font-face {
  font-family: MazzardH-SemiBold;
  src: url("../assets/font/MazzardH-SemiBold.ttf");
}
.font-tile{
  font-family: MazzardH-SemiBold;
  font-size: 32px;
}
.font-size-title {
  font-size: 50px;
}
.color-blue {
  color: #004e98;
}
</style>

