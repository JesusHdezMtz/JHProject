<template>
  <div class="background_home">
    
    <base-home id="home"></base-home>
    <base-profile id="profile"></base-profile>
    <base-briefcase id="briefcase"></base-briefcase>
    <base-contact id="contact"></base-contact>
    
  </div>
</template>

<script>
import BaseHome from "@/components/BaseHome.vue";
import BaseProfile from "@/components/BaseProfile.vue";
import BaseBriefcase from "@/components/BaseBriefcase.vue";
import BaseContact from "@/components/BaseContact.vue";

export default {
  components: {
    BaseHome,
    BaseProfile,
    BaseBriefcase,
    BaseContact,
  },
};
</script>

<style scoped>
.color-text{
  color: rgb(163, 163, 163);
}
.background_home {
  background: linear-gradient(
    to bottom,
    rgb(235, 235, 235) 0%,
    rgb(247, 247, 247) 8%,
    rgb(255, 255, 255) 100%
  );
}
</style>

