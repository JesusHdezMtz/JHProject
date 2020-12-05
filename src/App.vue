<template>
  <v-app>
  <base-header></base-header>

  <!-- Sizes your content based upon application components -->
  <v-main>

    <!-- Provides the application the proper gutter -->
    <v-container class="background-color"  fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

  <v-footer app>
    <!-- -->
  </v-footer>
</v-app>
</template>
<script>
import BaseHeader from "./components/BaseHeader";
export default {
  components: {
    BaseHeader,
  }
}
</script>
<style scoped>
.container{
  padding: 0px;
  margin: 0px;
}
.background-color{
  background-color: #EBEBEB;
}
</style>


