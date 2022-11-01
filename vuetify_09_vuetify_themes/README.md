09_vuetify_themes

1. vuetify gives us these keywords or classes for colors, things like orange, purple, etc and we can use those classes to colorise our different elements
2. but it also gives us a default theme, and this theme is basically a series of keywords again that we can use as classes, and they are success, error, warning, and info
3. we also have other keywords such as primary, secondary, and accent, .. but they are default theme colors,.. 
4. so if we use the class info, it is going to give us 
5. overriding theme colors, setting our own color for primary, secondary, success, error, .. etc
6. we can override this default theme inside the plugins folder, inside vuetify.js
7. when we use the vuetify plugin, the second parameter / object is some settings for our vuetify setup
8. and we have already set up iconfont as md for material design
9. now we can also specify here a theme, so this is an object, and this object can be used to control our different theme keywords
Vue.use(Vuetify, {
  iconfont: 'md',
  theme: {
    primary: '#9652ff',
    success: '#3cd1c2',
    info: '#ffaa2c',
    error: '#f83e70'
  }
})
10. changing class to primary in Navbar.vue
    <v-navigation-drawer v-model="drawer" app class="primary">
      <p>test</p>
    </v-navigation-drawer>
11. 