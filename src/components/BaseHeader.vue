<template>
  <div id="nav-bar">
    <v-app-bar app color="#F8F8F8"  elevate-on-scroll v-show="!isMobile()" >
      <v-tabs left color="grey" hide-slider>
        <a data-scroll href="#home" class="text-decoration-none color-text">
          <v-tab class="font-size-jesus ha-one">
            <v-icon class="pr-1" size="30" color="#2467b5"
              >mdi-account-box-outline</v-icon
            >
            JESÚS HERNÁNDEZ
          </v-tab>
        </a>
      </v-tabs>

      <v-tabs centered color="grey" hide-slider > 
        <a
          v-for="(item, i) in links"
          :key="i"
          data-scroll
          :href="item.link"
          class="text-decoration-none color-text"
        >
          <v-tab class="ha-two">
            <v-icon class="pr-2" size="18" color="#2467b5">{{
              item.icon
            }}</v-icon>
            {{ item.name }}
          </v-tab>
        </a>
      </v-tabs>
    </v-app-bar>

    <v-app-bar app color="#F8F8F8"  elevate-on-scroll  width="100%" v-show="isMobile()">
      <div class="d-flex">
        <a href="#home" class="text-decoration-none color-text">
          <v-tabs background-color="#F8F8F8" left color="grey" hide-slider>
            <v-tab class="pl-0 font-size-jesus-xs color-text">
              <v-icon class="pr-1" size="30" color="#2467b5"
                >mdi-account-box-outline</v-icon
              >
              JESÚS HERNÁNDEZ
            </v-tab>
          </v-tabs>
        </a>
      </div>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon
        right
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-app-bar>

    <v-navigation-drawer v-model="drawer" height="500" width="100%" class="background-color-gray accent-4"
       fixed floating bottom>
      <v-list >
        <v-subheader class=""><strong>JESÚS HERNÁNDEZ</strong></v-subheader>
        <v-divider></v-divider>
        <a
          class="text-decoration-none color-text"
          v-for="(item, i) in links"
          :key="i"
          :href="item.link"
          @click="drawerfalse"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon size="black" color="#2467b5">{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title class="color-text">{{ item.name }}</v-list-item-title>
          </v-list-item>
        </a>
      </v-list>
      <template v-slot:append>
        <div class="pa-2">
          <v-btn block color="orange" dark @click="drawerfalse">
            CERRAR
          </v-btn>
        </div>
      </template>
    </v-navigation-drawer>
  </div>
</template>


<script>
var SmoothScroll = require("smooth-scroll");
var scroll = new SmoothScroll('a[href*="#"]', {
  speed: 800,
  speedAsDuration: true,
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
    drawer: false,
    group: null,
  }),

  methods: {
    isMobile: function () {
      return this.$vuetify.breakpoint.smOnly || this.$vuetify.breakpoint.xsOnly;
    },
    drawerfalse: function () {
      this.drawer = false;
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
.color-text {
  color: rgb(100, 100, 100);
}
.font-size-jesus {
  font-size: 23px;
}
.ha-one{
  height: 100%;
}
.ha-two{
  height: 100%;
  width: 100%;
}
.background-color-gray{
  background-color: #F8F8F8;
}
</style>