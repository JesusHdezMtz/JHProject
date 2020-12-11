<template>
  <div class="pt-16">
      <v-row class="mx-0 pt-10">
        <v-col cols="12" xs="12" sm="6" md="6" lg="6" xl="6">
          <div class="px-5 pt-15 d-flex align-content-center flex-wrap">
            <h1 class="color-blue font-tile">Ingeniero De Software</h1>
            <v-col cols="12" class="pa-0 ma-0">
              <h1 class="font-size-title font-tile color-orange">
                JESÚS HERNÁNDEZ
              </h1>
            </v-col>

            <h3 class="text-justify">
              Egresado de la licenciatura de ingeniería de software de la
              Universidad Veracruzana, co-fundador de Arcup (arcup.com.mx),
              desarrollador front-end y back-end.
            </h3>
            <h3 class="pt-2">
              <v-icon class="pr-0" size="27" color="#FF6700"
                >mdi-email-outline
              </v-icon>
              jesus.hdez@arcup.com.mx
            </h3>

          </div>
        </v-col>
        <v-col cols="12" xs="12" sm="6" md="6" lg="6" xl="6">
          <v-img
            class="ml-1"
            max-width="100%"
            max-height="100%"
            src="../assets/view-home/image-1.png"
          >
          </v-img>
        </v-col>
      </v-row>
    </div>
</template>
<style  scoped>
@font-face {
  font-family: MazzardH-SemiBold;
  src: url("../assets/font/MazzardH-SemiBold.ttf");
}
.font-tile {
  font-family: MazzardH-SemiBold;
  font-size: 28px;
}
.font-size-title {
  font-size: 45px;
}
.font-size-jesus {
  font-size: 23px;
}
.color-blue {
  color: #004e98;
}
.color-orange {
  color: #ff6700;
}
</style>