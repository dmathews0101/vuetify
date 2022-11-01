06_vuetify_breakpoints_and_visibility

1. breakpoints are typically width values in pixels, which represent the width of different devices or viewports, which we might view the website on
2. and at these breakpoints, we typically rearrange layout of our site content if we need to, to fit into that device width nicely
3. so, for example, we might have a breakpoint for small screen sizes, which is going to be roughly 400 to 500 pixels, and this would target everyone viewing the website on a mobile phone for example
4. so at this breakpoint, we might want to say, rearrange the content this way, or show and hide these elements, etc
5. we might also have a breakpoint at about 700 to 800 pixels for certain tablets, and we use that breakpoint to rearrange or show and hide content for those devices, etc,.. and it goes all the way up to large screens
6. so vuetify comes with a predefined set of breakpoints and helper classes, which allow us to do a certain things at those different breakpoints, 
7. for example, if we want to make things visible on a desktop, but not on a mobile, for that we would use one of vuetify's breakpoints and a visibility class
8. the different breakpoints that the vuetify comes baked with are : xs, sm, md, lg, xl
9. so, these are the different codes that we can use in our different classes
10. visibility: if we want to show something on desktops but not on mobiles, then we would use a visibility class, and it follows this format : hidden-{breakpoint}-{condition}
11. so for example : if we only want to show something on extra small devices, we would say : hidden-xs-only
12. hiding a button on medium sized screens, at that break point and down,.. so anything less than this,.. so small screens and extra small screens as well 
<v-btn class="hidden-md-and-down">click me 1</v-btn>
13. to not show a button for medium sized screens, large and extra large, .. but we do want to show it on anything less than medium
<v-btn class="hidden-md-and-up">click me 2</v-btn>
it shows up only on sm and xs screens,.. hidden on md, lg, and xl screens
14. to have a button hidden on small screen only,.. not extra small - mobiles, just small - which is things like tablets
<v-btn class="hidden-sm-only">click me 3</v-btn>
so only for this period in between extra small and medium, - for small screens - it disappears
14. summary : visibility and different breakpoints that vuetify employs inside our projects 