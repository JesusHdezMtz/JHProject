<template>
  <div id="footer">
      <v-footer color="#120d3b" padless>
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="(item, i) in links"
        :key="i"
        color="white"
        text
        rounded
        class="my-2"
      >
       <a :href="item.link" class="text-decoration-none white--text">
        <v-icon class="pr-2" size="18" color="#FF6700">{{ item.icon }}</v-icon>
        {{ item.name }}
        </a>
      </v-btn>
      <v-col
        class="background-footer-color-secondary py-4 px-0 text-center white--text"
        cols="12"
      >
        <div class="font-size-footer mx-16">
          <v-icon class="pr-2" size="18" color="#FF6700">mdi-email-outline</v-icon>
          jesus.hdez@arcup.com.mx
          <v-icon class="pr-2 pl-2" size="18" color="#FF6700">mdi-phone</v-icon>
          (+52) 2281132016
        </div>
      </v-col>
      <v-col class="py-4 text-center white--text" cols="12">
        <strong>{{ new Date().getFullYear() }} | Jesús Hernández</strong>
      </v-col>
    </v-row>
  </v-footer>
    </div>
</template>

<script>
var SmoothScroll = require('smooth-scroll');
const scroll = new SmoothScroll('a[href*="#"]', {
  speed: 800,
  speedAsDuration: true
});

export default {
  data: () => ({
    links: [
      {
        link: "#home",
        name: "INICIO",
        icon: "mdi-home",
      },
      {
        link: "#profile",
        name: "PERFIL",
        icon: "mdi-account",
      },
      {
        link: "#briefcase",
        name: "PORTAFOLIO",
        icon: "mdi-folder-multiple-image",
      },
      {
        link: "#contact",
        name: "CONTACTO",
        icon: "mdi-email-outline",
      },
    ],
  }),

};
</script>
