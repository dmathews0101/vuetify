08_vuetify_navigation_drawers

1. adding a button to toolbar to open the navigation drawer 
2. adding v-toolbar side icon
<v-toolbar-side-icon class="grey--text" @click="drawer = !drawer"></v-toolbar-side-icon>
3. adding navigation drawer
<v-navigation-drawer v-model="drawer" app class="indigo">
  <p>test</p>
</v-navigation-drawer>