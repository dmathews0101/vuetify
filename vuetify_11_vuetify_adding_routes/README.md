11_vuetify_adding_routes

1. before looking at any more vuetify components, what we can do is take a quick sidestep, and set up these different routes
2. one for projects, homepage for dashboard and one for team
3. renaming home component to dashboard
4. we also want a route/component for the project, so renaming about.vue to projects.vue
5. setting up routes :
import Vue from 'vue'
import Router from 'vue-router'
import Dashboard from './views/Dashboard.vue'
import Projects from './views/Projects'
import Team from './views/Team'

Vue.use(Router)

export default new Router({
  mode: 'history',
  base: process.env.BASE_URL,
  routes: [
    {
      path: '/',
      name: 'dashboard',
      component: Dashboard
    },
    {
      path: '/projects',
      name: 'projects',
      component: Projects
    },
    {
      path: '/team',
      name: 'team',
      component: Team
    }
  ]
})
6. Making changes to components :
we do this just in case we want to style anything in this template later on, we have got a css class we can hook on to there, which contains everything inside the projects.
---
Dashboard.vue
<template>
  <div class="dashboard">
    <h1>Dashboard</h1>
  </div>
</template>

<script>
export default {
};
</script>
---
Projects.vue
<template>
  <div class="projects">
    <h1>Projects</h1>
  </div>
</template>

<script>
export default {};
</script>
---
Team.vue
<template>
  <div class="team">
    <h1>Team</h1>
  </div>
</template>

<script>
export default {};
</script>
---
7. so now we have these three routes set up- dashboard, projects and team route,.. now these are the routes that we have to go to, to load in those components
8. so now these are also hooked up into our Navbar.vue --> router :to="link.route"