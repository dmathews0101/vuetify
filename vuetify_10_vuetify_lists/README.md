10_vuetify_lists

1. outputting links inside this navigation using list component
2. we are going to use the list components and a combination of different sub components inside that list to output some links on the navigation drawer
3. now, each link is going to have a title, the name of the link, and it is also going to have a little icon on the left
4. first we have to do is create the actual list component, the thing that surrounds the list,
5. we can think of this as the ul tag in html, and that is called v-list
6. inside the list, we need several different list items,.. in vuetify they are called list tiles
7. we can think of this as li tags, .. now inside this component, we can nest other components which output different things inside the list tile, 
8. first thing we can do is output the tile content, and that is any kind of text
9. all of this is going to configure all of our list items for us and style them, so that we dont have to do any extra legwork
10. links: [
        { icon: "dashboard", text: "Dashboard", route: "/" },
        { icon: "folder", text: "My Projects", route: "/projects" },
        { icon: "person", text: "Team", route: "/team" },
      ],
11. so each link is an object, and each object contains three properties,.. we have an icon-(dashboard, folder, person), text-(Dashboard, My Projects, Team) and route-( /, /projects, /team)
12. so now what we want to do is take this data and cycle through that data
13. looping through a data property:
    <v-navigation-drawer v-model="drawer" app class="primary">
      <v-list>
        <v-list-tile v-for="link in links" :key="link.text">
          <v-list-tile-action>
            <v-icon class="white--text">{{ link.icon }}</v-icon>
          </v-list-tile-action>
          <v-list-tile-content>
            <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
          </v-list-tile-content>
        </v-list-tile>
      </v-list>
    </v-navigation-drawer>
14. what we also want to do is attach the router to each one of these, so that when we click on these, it goes to a specific route, .. and those routes are defined by the route property in the links object
15. if we wanted to use the router on a particular element, all we needed to do is add it as a prop to the element that we are using in vuetify, 
16. so we can add it to the list tile,.. we want this tile to use the router, so when someone clicks on this we are going to invoke the router and take them somewhere else, then we use the to prop to say where we want to go to
17. now in this case, we want to bind some data to this property, because the data we want is the link.route, so we can bind it using the :to="link.route", 
18. so now, each tile is going to link to its own link route, whether that would be /, /projects or /team
<v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
19. we also get this nice hover effect, because we are using the router prop here
20. extra: setting up the routes and setting up the components for those routes