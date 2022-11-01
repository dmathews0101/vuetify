vuetify_12_vuetify_padding_and_margin

1. (spacing)-padding and margin in vuetify works by using css classes, and they follow the structure {property}{direction}-{size}
2. property (m-margin, p-padding)
say for example we want to create a class which is going to control the margin, the first property for us would be m, then it is the direction
3. direction would be where do we want to apply this margin or padding, do we want it to the 
t-top, 
b-bottom, 
l-left, 
r-right, 
x-x direction-applies spacing to the left and the right, 
y-y direction-top and bottom, 
a-all directions
4. for example, if we want to apply a margin to the left and right of an element, then we would say,
mx-size of the margin
5. size can be anything between 0 and 5.
it uses the $spacer variable to control the size of the margin and multiplies it by 0, 0.25, .5, 1, 1.5, 3
example : mx-3, and that would give us a margin of strength 3 in the x direction, so left and right
6. same is true for the padding, 
7. if we wanted to apply padding in all directions to a strength of 2, then it would be p, a for all : pa-2
8. to add padding to h1 inside team, dashboard and projects vue file, we can go to app.vue and just apply a margin to v-content, which is going to move whatever is nested inside router-view
9. so we just have to do it once, and every single page will get that margin
<v-content class="mx-4 mb-4"
,..mb-4 to apply a margin bottom of 4
10. we can apply the padding and margin to the main content as well,.. at the minute, we are just applying the padding and margin only to h1 at the top
11. later content will be created using the grid system, and whenever we use a grid,.. we generally place it inside a container element, and a container element keeps everything within a central width on the page, and it also helps to structure our content for different screensizes
12. we create a container by using 
<v-container class="my-5">content</v-container>
13. if we want to apply a margin to this content at the top, to bring it down, to do this, we have to give it a class my-5
14. when we make the screen smaller, makes a jump and makes the central column smaller,.. then it gets to a certain point where it just goes to a 100 percent width