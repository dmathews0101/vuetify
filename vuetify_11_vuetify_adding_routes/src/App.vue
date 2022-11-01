<template>
  <v-app class="grey lighten-4">
    <Navbar />
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>

<script>
// @/ gives us the root directory of the src folder
import Navbar from "@/components/Navbar";

export default {
  name: "App",
  components: { Navbar },
  data() {
    return {};
  },
};
</script>
