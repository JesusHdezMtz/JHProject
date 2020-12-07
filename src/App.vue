<template>
  <v-app>
  <base-header></base-header>

  <!-- Sizes your content based upon application components -->
  <v-main class="background-title pt-1">

    <!-- Provides the application the proper gutter -->
    <v-container class="background-title"   fluid>

      <!-- If using vue-router -->
      <router-view></router-view>
    </v-container>
  </v-main>

  <base-footer></base-footer>
</v-app>
</template>
<script>
import BaseHeader from "./components/BaseHeader";
import BaseFooter from "./components/BaseFooter";
export default {
  components: {
    BaseHeader,
    BaseFooter,
  }
}
</script>
<style scoped>
.container{
  padding: 0px;
  margin: 0px;
}

.background-title {
  background: linear-gradient(
    to bottom,
    rgb(235, 235, 235) 0%,
    rgb(255, 255, 255) 100%
  );
}
</style>


