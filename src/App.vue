<template>
  <v-app>
    <base-header></base-header>
    <router-view></router-view>
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
  },
};
</script>
<style scoped>
.container {
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


