<template>
  <div class="py-10 text-center background-color">
    <div class="heigt"></div>
    <div class="px-10">
      <v-avatar size="250" class="border-avatar">
      <img src="../assets/view-profile/photo-jesus.jpg" alt="Jesús Hernández" />
    </v-avatar>
    <h2 class="font-tile pt-5 color-orange">Jesús Hernández</h2>
    <h3 class="font-size-subtitle white--text">Ingeniero de software</h3>
    <h3 class="font-size-subtitle white--text">
      Desarrollador Front-End y Back-End
    </h3>
    <h3 class="font-size-subtitle white--text">
      Co-Fundador de <span class="color-orange">Arcup.com.mx</span>
    </h3>
    </div>
    
  </div>
</template>
<style scoped>
.heigt {
  height: 50px;
}
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
.font-size-subtitle {
  font-family: MazzardH-SemiBold;
  font-size: 23px;
}
.background-color {
  background-color: #120d3b;
  background-image: url("../assets/view-home/image-2.png");
  background-size: cover;
}
.color-blue {
  color: #004e98;
}
.color-orange {
  color: #ff6700;
}
.border-avatar {
  border-style: solid;
  border-color: #ff6700;
  border-width: 5px;
}
</style>
