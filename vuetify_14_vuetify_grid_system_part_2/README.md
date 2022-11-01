vuetify_13_vuetify_the_grid_system_part_1

1. vuetify uses the flexbox under the hood to create this 12 column grid for us in which we can lay out our content
2. now, flexbox is purely a vanilla css mechanism, which allows us to create this grid like layouts very very easily
3. vuetify just abstracts a little away from the css and it adds in all of this functionality into its grid components
4. with this vuetify flexbox grid, we can easily make different layouts and they are responsive as well
5. 12 column layout or a 12 column grid means that our horizontal space left to right is split up into 12 equal columns of width
6. now, imagine we have 12 different elements that we want to spread across on the page, now if we wanted them all to be on one row, then we would assign each element one column of width like this, and if we counted these there would be 12 
7. so they would all be spaced equally on the page, 
other options:
2 columns in width, for each of these elements
3 columns in width
4 columns in width
6 columns in width
12 columns in width
8. now, we use this grid system and these different columns to lay out our content in the page,.. it is not always going to look like this,.. so for example, say we have an image on the left and some text on the right, now we might want the image to take up 4 columns in width on the left, but the text on the right, we might want to take up 8 columns of width, and thats fine because 8+4 is 12, and that takes up all the space available to us
9. so if we watch this, we will notice that, this is also responsive, it just kind of goes down into these different sizes, but, if we scroll down here, we are going to see some different versions of this grid, like this,.. if we make this a little bigger, we can see that we have two at the top, then 3, then 4
10. now if we make this a little smaller now, like so, then we can see that it has gone on to 4 different rows,.. so now we have 2, 3, 2 and 2,.. before it was 2, 3 and 4 at the bottom,.. so it has rearranged this based on the screen size
11. so it is very flexible, .. used throughout the series to lay out content on our pages
12. making a grid --> Dashboard.vue
-> grid inside v-container
-> create a layout, and a layout basically represents a row of content
--> so we use a component called v-layout to do this, now then, we want to specify that this is going to be a row of content, we can also use column and that would use flexbox vertically for us,.. we can think of this as a row of elements,.. we are making a row on the grid
--> now then, inside here we need to use elements or components called v-flex, and they are the elements which are going to be placed into these different positions on that row on the grid. we can see this as a container element for certain element on this row. they represent these different positions
-->now, these v-flex elements, they can have different props, which tell it how to space out the content on the screen
--> breakpoints - xs, s, m, l, xl
--> now what we can do is say, okay, at xs(extra small) screens, I want you to take up six columns of width, or 12 columns of width, or 4, or whatever we want
--> and we always start with the mobile, it is always a good idea to do that, so you go with a mobile first approach and it looks good on a mobile and then you're extending it to larger screens
--> xs is not a class but a prop, at this sized screen, we want this flex item, this v-flex component to take up 12 columns of width, so we say xs12
--> now then, when it gets to a medium sized screen, we want this to be 6 columns of width instead because we dont need it to be full width on a medium sized screen, we have more room, so we can be happy with half of the width which is md6
--> so at xs screens and small screens, it is going to be 12, when it reaches md sized, it is going to be 6 columns of width,
13. laying out elements using the grid system :
<template>
  <div class="dashboard">
    <h1 class="subheading grey--text">Dashboard</h1>
    <v-container class="my-5">
      <v-layout row wrap>
        <v-flex xs12 md6>
          <v-btn outline block class="primary">1</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outline block class="primary">2</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outline block class="primary">2</v-btn>
        </v-flex>
        <v-flex xs4 md2>
          <v-btn outline block class="primary">2</v-btn>
        </v-flex>
      </v-layout>
    </v-container>
  </div>
</template>
14. another example to show us some of the spacing options, .. not taking up the full width of the available space in the row,.. it's fine to not take up the whole row of space
15. however, if we have just 2 elements, we might want to position them differently, for example, we might want to put them in the center, or we might want to put them to the right, etc
16. we can control that behaviour by adding props to v-layout component, this row 
17. so there is many different props we can use, the first one we can check is justify-space-around,.. if we save this now, what is going to happen is it is going to justify them in the center and space around them
---
      <v-layout row wrap justify-space-around>
        <v-flex xs4 md3>
          <v-btn outline block class="success">1</v-btn>
        </v-flex>
        <v-flex xs4 md3>
          <v-btn outline block class="success">2</v-btn>
        </v-flex>
      </v-layout>
    </v-container>
---
we could also say :
--> justify-center - that puts them in very middle without spacing between them, but space on the left and right
--> justify-end - that is going to put them at the end
--> justify-space-between - that is going to just put space between them and we have one on the left and one on the right, so no space on the outer edges
--> that is how we move it around on the screen as well, if we dont take up all the available space
18. extra -- using grid system to layout components for the project