02_setting_up_vuetify

1. to create a new vue application using vuecli3, 
vue create vuetify-app 
2. we have to select a preset 
--> Manually select features
--> Babel, Router, Linter / Formatter
3. use history mode for router? Y (to prevent # sign inside url)
4. pick a linter / formatter config: 
--> ESLint with error prevention only
5. Pick additional lint features: 
--> Lint on save
6. where do you prefer placing config for Babel, ESLint, etc.? 
--> in package.json
7. save this as a preset for future projects? (y/N) N
8. after pressing enter, this is going to install the project for us now
9. project folder created, cd into this directory,  
10. npm run serve, to run local development server
11. what we want to do next is install vuetify, the way we do that is by adding a plugin into this vue application
12. so plugins are the way forward inside the vue CLI version 3 
13. to add a plugin
vue add vuetify
14. so this is going to add the vuetify plugin for us now, and ask us a couple of questions to set up this plugin
---
15. choose a preset
Default (recommended)
16. what this plugin does, is edit our files inside this project
17. new plugins folder--> inside vuetify.js
import Vue from 'vue';
import Vuetify from 'vuetify/lib';

Vue.use(Vuetify);

export default new Vuetify({
});

this just registers vuetify as a plugin, so we can see we import vue, vuetify then using vuetify plugin, this is how we register a plugin in vuejs
18. what this is doing now is giving us the ability to use all of vuetify's custom components inside our vue application
import 'vuetify/src/stylus/app.sty1'

Vue.use(Vuetify, {
    iconfont: 'md',
})
the second object right here just represents some options for vuetify, one of the properties is the iconfont, and md is material design
19. it has also edited our different files, in app.vue, we have a different template and these different components and all these components start with v-, and that stands for vuetify- then the component name
20. npm run serve 
or
yarn serve
21. now the app uses the different vuetify components inside the template 
22. summary: adding vuetify to project