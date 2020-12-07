<template>
  <v-footer color="#120d3b" padless>
    <v-row justify="center" no-gutters>
      <v-btn
        v-for="(item, i) in links"
        :key="i"
        @click="openView(item.link)"
        color="white"
        text
        rounded
        class="my-2"
      >
        <v-icon class="pr-2" size="18" color="#FF6700">{{ item.icon }}</v-icon>
        {{ item.name }}
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
</template>

<script>
export default {
  data: () => ({
    links: [
      {
        link: "Home",
        name: "INICIO",
        icon: "mdi-home",
      },
      {
        link: "Profile",
        name: "PERFIL",
        icon: "mdi-account",
      },
      {
        link: "Briefcase",
        name: "PORTAFOLIO",
        icon: "mdi-folder-multiple-image",
      },
      {
        link: "Contact",
        name: "CONTACTO",
        icon: "mdi-email-outline",
      },
    ],
  }),
  methods: {
    openView: function (view) {
      this.$router.push({ name: view }).catch(() => {});
    },
  },
};
</script>

<style>
.background-footer-color-secondary {
  background-color: #120d3b;
}
.font-size-footer {
  font-size: 14px;
}
</style>