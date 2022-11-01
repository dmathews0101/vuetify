05_vuetify_button_and_icons_or

1. first vuetify component : button
2. button with class
<v-btn class="pink white--text">click me</v-btn>
3. button with color
<v-btn dark color="pink">click me</v-btn>
we can also color certain elements/components using this color prop, instead of using the classes..
4. we can use the color="pink" prop to control the color of the button as well, instead of using this as a class
5. depressed button - pushed back against the page, so it removes the shadow
<v-btn dark depressed color="pink">click me</v-btn>
6. flat button - removes drop shadow, makes background transparent
<v-btn flat depressed color="pink">click me</v-btn>
when we apply a flat prop to a button, this color prop, instead of controlling the background, because the background is now transparent, because of the flat prop, this color prop now controls the text color and the hover color, when we hover over the button
7. v-icon - uses material design icon by default
 <v-btn flat class="pink white--text">
      <v-icon left>email</v-icon>
      <span>email me</span>
 </v-btn>
 ---
 modifications:
 text prop instead of flat
 mdi-email for email icon
 ---
 
if google material icons are not working -- 3 steps
a. npm install material-design-icons-iconfont --save
b. in main.js > import 'material-design-icons-iconfont/dist/material-design-icons.css'
c. in vuetify.js > 
export default new Vuetify({
  iconfont: 'md',
});

no need to write mdi in front of the keyword, 
only have to write the keyword as it is written on the material.io/resources/icons/
---
8. small button and icon
    <v-btn depressed small class="pink white--text">
      <v-icon left small>email</v-icon>
      <span>email me</span>
    </v-btn>
9. large button and icon
    <v-btn depressed large class="pink white--text">
      <span>email me</span>
      <v-icon right large>email</v-icon>
    </v-btn>
10. favorite button
    <v-btn fab depressed small dark color="purple">
      <v-icon>favorite</v-icon>
    </v-btn>