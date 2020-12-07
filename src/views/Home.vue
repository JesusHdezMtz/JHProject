<template>
  <div class=" background_home">
    <v-card color="rgb(235, 235, 235)" flat :height="height"></v-card>
    <v-row class="mx-0">
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
          <v-col cols="12" class="mx-0 px-0">
            <v-btn class="mx-0" dark color="#004e98"> Contactar </v-btn>
          </v-col>
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
    <div class="text-center pa-15">
      <v-icon class="pt-10" size="50" color="#004e98"
        >mdi-account-group
      </v-icon>

      <h1 class="font__main-alter">TECNOLOGÍAS</h1>
      <v-card
        
        flat
        height="3"
        color="#004e98"
        width="300"
        class="mx-auto"
      >
        <h3 class="pt-1">Explora las herramientas de trabajo</h3></v-card
      >
    </div>
    <div>
      <div class="d-flex align-center text-center justify-center">
      </div>
      <v-row class="mx-0 mb-15">
        <v-col
          v-for="(item, index) in cards"
          :key="index"
          cols="12"
          sm="4"
          md="4"
          lg="4"
          xs="12"
          v-intersect="{
          handler: onIntersect,
          options: {
            threshold: [0, 0.5, 1.0],
          },
        }"
        >
          <transition name="slide-fade">
            <v-card class="mx-auto" elevation="5" max-width="90%" height="100%" v-show="isIntersecting">
              <v-img
                :src="item.img"
                height="200px"
              ></v-img>

              <v-card-title>{{item.title}}</v-card-title>

              <v-card-subtitle>{{item.subtitle}}</v-card-subtitle>

              <v-card-actions>
                <v-btn color="orange lighten-2" text> Explore </v-btn>

                <v-spacer></v-spacer>

                <v-btn icon @click="show = !show">
                  <v-icon>{{
                    show ? "mdi-chevron-up" : "mdi-chevron-down"
                  }}</v-icon>
                </v-btn>
              </v-card-actions>

              <v-expand-transition>
                <div v-show="show">
                  <v-divider></v-divider>

                  <v-card-text>
                    I'm a thing. But, like most politicians, he promised more
                    than he could deliver. You won't have time for sleeping,
                    soldier, not with all the bed making you'll be doing. Then
                    we'll go with that data file! Hey, you add a one and two
                    zeros to that or we walk! You're going to do his laundry?
                    I've got to find a way to escape.
                  </v-card-text>
                </div>
              </v-expand-transition>
            </v-card>
          </transition>
        </v-col>
      </v-row>
    </div>
  </div>
</template>

<script>
export default {
  data: () => ({
    isIntersecting: false,
    show: false,
    cards: [
      {
        img: "https://miro.medium.com/max/2430/1*ACR0gj0wbx91V_xgURifWg.png",
        title: "Vue Js",
        subtitle: "Framework de JavaScript de código abierto para la construcción de interfaces de usuario y aplicaciones de una sola página.",
        icon: "mdi-home",
        txt: "",
      },
      {
        img: "https://miro.medium.com/max/2264/1*8o5BkjShcL3f9fqL3zwLaA.png",
        title: "Vuetify",
        subtitle: "Vuetify es un framework que combina la potencia del popular VueJs con la estética de Material Design.",
        icon: "mdi-home",
        txt: "",
      },
      {
        img: "https://www.psdahtmlpasoapaso.com/blog/wp-content/uploads/2013/04/html5css3.png",
        title: "HTML y CSS",
        subtitle: "HTML es un lenguaje de marcado que se utiliza para el desarrollo de páginas de Internet. CSS es lo que se denomina lenguaje de hojas de estilo en cascada.",
        icon: "mdi-home",
        txt: "",
      },
    ],
  }),
  methods: {
    onIntersect(entries, observer) {
      if(!this.isIntersecting){
         this.isIntersecting = entries[0].intersectionRatio >= 0.5;
         
      }
    },
  },
  computed: {
    height() {
      switch (this.$vuetify.breakpoint.name) {
        case "xs":
          return 0;
        default:
          return 100;
      }
    },
  },
};
</script>

<style scoped>
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
.color-blue {
  color: #004e98;
}
.color-orange {
  color: #ff6700;
}
.background-title {
  background: linear-gradient(
    to bottom,
    rgb(235, 235, 235) 0%,
    rgb(255, 255, 255) 100%
  );
}
.slide-fade-enter-active {
  transition: all 5s ease;
}
.slide-fade-leave-active {
  transition: all 0.1s cubic-bezier(1, 0.5, 0.8, 1);
}
.slide-fade-enter,
.slide-fade-leave-to {
  transform: translateY(30px);
  opacity: 0;
}
.background_home {
  background-image: url("../assets/view-home/image-2.png");
  background-size: cover;
  background-position-x: center;
}
</style>

