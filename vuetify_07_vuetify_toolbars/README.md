07_vuetify_toolbars

1. making todo application : starting by creating a toolbar,
no in the home page because then it would only show on the home page instead, what we are going to do is create a seperate component for this, and nest that inside App.vue
2. inside components folder --> create Navbar.vue
3. now we have to import this inside App.vue
import Navbar from "@/components/Navbar";
4. we also have to register it in App.vue
export default {
  name: "App",
  components: { Navbar },
  data() {
    return {};
  },
};
5. so now we can nest it in the template --> App.vue -->
<template>
  <v-app>
    <Navbar />
    <v-content>
      <router-view></router-view>
    </v-content>
  </v-app>
</template>
6. adding a toolbar in Navbar.vue,.. some of the different options for toolbar
7. a toolbar in vuetify is much like a menu bar, and we see them at the top of the websites with links and logos in
8. the way we create one is by using the v-toolbar component
9. changing background color for app in App.vue
10. toolbar title
    <v-toolbar flat app>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Todo</span>
        <span>Ninja</span>
      </v-toolbar-title>
    </v-toolbar> 
11. navbar with sign out button and v-spacer
  <nav>
    <v-toolbar flat app>
      <v-toolbar-title class="text-uppercase grey--text">
        <span class="font-weight-light">Todo</span>
        <span>Ninja</span>
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn flat color="grey">
        <span>Sign Out</span>
        <v-icon right>exit_to_app</v-icon>
      </v-btn>
    </v-toolbar>
  </nav>
12. extra : navigation drawer