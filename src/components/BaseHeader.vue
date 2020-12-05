<template>
  <div>
    <v-app-bar app color="#F8F8F8" flat elevation="3" v-show="!isMobile()">
        <v-tabs left color="grey" hide-slider>
          <v-tab class="font-size-jesus" @click="openView('Home')">
            <v-icon class="pr-1" size="30" color="#2467b5"
              >mdi-account-box-outline</v-icon
            >
            JESÚS HERNÁNDEZ
          </v-tab>
        </v-tabs>

      <v-tabs right color="grey" hide-slider>
        <v-tab v-for="(item, i) in links" :key="i" @click="openView(item.link)">
          <v-icon class="pr-2" size="18" color="#2467b5">{{ item.icon }}</v-icon>
          {{ item.name }}
        </v-tab>
      </v-tabs>
    </v-app-bar>

    <v-toolbar color="#F8F8F8" v-show="isMobile()">
      <div class="d-flex">
        <router-link :to="{ name: 'Home' }" class="text-decoration-none">
          <v-tabs background-color="#F8F8F8" left color="grey" hide-slider>
            <v-tab class="pl-0 font-size-jesus-xs">
              <v-icon class="pr-1" size="30" color="#2467b5"
                >mdi-account-box-outline</v-icon
              >
              JESÚS HERNÁNDEZ
            </v-tab>
          </v-tabs>
        </router-link>
      </div>
      <v-spacer></v-spacer>
      <v-app-bar-nav-icon
        right
        @click.stop="drawer = !drawer"
      ></v-app-bar-nav-icon>
    </v-toolbar>

    <v-navigation-drawer v-model="drawer" absolute left>
      <v-list>
        <v-subheader>CONTÁCTANOS</v-subheader>
        <v-divider></v-divider>
        <router-link
          v-for="(item, i) in links"
          :key="i"
          :to="{ name: item.link }"
          class="text-decoration-none"
        >
          <v-list-item>
            <v-list-item-icon>
              <v-icon size="black" color="black">{{ item.icon }}</v-icon>
            </v-list-item-icon>
            <v-list-item-title>{{ item.name }}</v-list-item-title>
          </v-list-item>
        </router-link>
      </v-list>
    </v-navigation-drawer>
  </div>
</template>


<script>
export default {
  name: "BaseHeader",
  data: () => ({
    links: [
      {
        link: "Home",
        name: "INICIO",
        icon: "mdi-home",
      },
      {
        link: "About",
        name: "PERFIL",
        icon: "mdi-account",
      },
      {
        link: "About",
        name: "PORTAFOLIO",
        icon: "mdi-folder-multiple-image",
      },
      {
        link: "About",
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
    openView: function (view){
      this.$router.push({ name: view }).catch(()=>{});
    },
  },
};
</script>

<style scoped>
.font-size-jesus {
  font-size: 23px;
}
.font-size-jesus-xs {
  font-size: 18px;
}
.background-header{
    background-color: #F8F8F8;
}
</style>