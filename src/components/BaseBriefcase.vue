<template>
  <div class="background-color pb-15">
    <div class="text-center py-16">
      <v-icon class="pt-10" size="50" color="#004e98"
        >mdi-account-group
      </v-icon>

      <h1 class="font__main-alter">PROYECTOS</h1>
      <v-card flat height="3" color="#004e98" width="300" class="mx-auto">
      </v-card>
      <h3 class="pt-1">Explora los ultimos proyectos realizados</h3>
    </div>
    <div>
      <div class="d-flex align-center text-center justify-center"></div>
      <v-row class="mx-0 mb-15">
        <v-col
          v-for="(itemCard, index) in itemCards"
          :key="index"
          cols="12"
          sm="12"
          md="12"
          lg="12"
          xs="12"
          v-intersect="{
            handler: onIntersect,
            options: {
              threshold: [0, 0.5, 1.0],
            },
          }"
        >
          <transition name="slide-fade">
            <v-card
              elevation="10"
              max-width="900"
              class="mx-auto border-card"
              v-show="isIntersecting"
            >
              <v-carousel
                continuous
                cycle
                hide-delimiter-background
                height="400"
              >
                <v-carousel-item
                  v-for="(imgCarousel, i) in itemCard.itemsCarousel"
                  eager
                  elevation="10"
                  :key="i"
                  :src="imgCarousel.src"
                ></v-carousel-item>
              </v-carousel>
              <v-card-title>{{ itemCard.title }}</v-card-title>

              <v-card-subtitle>{{ itemCard.subtitle }}</v-card-subtitle>

              <v-card-actions>
                <v-btn color="orange lighten-2" text>
                  <a class="text-decoration-none orange--text" :href="itemCard.link"
                    >Explorar
                  </a>
                </v-btn>

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

                  <v-card-text class="text-justify">
                    {{ itemCard.description }}
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
import img1 from "../assets/projects/arcup/img1.png";
import img2 from "../assets/projects/arcup/img2.png";
import img3 from "../assets/projects/arcup/img3.png";
import img4 from "../assets/projects/arcup/img4.png";

export default {
  data: () => ({
    isIntersecting: false,
    show: false,
    itemCards: [
      {
        title: "Arcup",
        subtitle: "Empresa de Desarrollo de Software",
        itemsCarousel: [
          {
            src: img1,
          },
          {
            src: img2,
          },
          {
            src: img3,
          },
          {
            src: img4,
          },
        ],
        description:
          "Arcup es una empresa emergente de desarrollo de software basada en las nuevas " +
          "tendencias tecnológicas. Utilizando procesos metódicos y diseños modernos, planea colocarse" +
          " como una empresa referente en el área de la informática.",
        link: "https://arcup.com.mx/"
      },
    ],
  }),

  methods: {
    onIntersect(entries, observer) {
      if (!this.isIntersecting) {
        this.isIntersecting = entries[0].intersectionRatio >= 0.5;
      }
    },
  },
};
</script>

<style scoped>
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
.border-card {
  border-style: solid;
  border-color: rgb(255, 255, 255);
  border-width: 5px;
}
.background-color {
  background-image: url("../assets/view-home/image-3.png");
  background-size: cover;
}
</style>

