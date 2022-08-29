

# Learn Typography by Building a Nutrition Label, Completed

> - Typography is the art of styling your text to be easily readable and suit its purpose.
> - In this course, you'll use typography to build a nutrition label webpage. You'll learn how to style text, adjust line height, and position your text using CSS.
---

> **Step 1** <br>
We've provided a basic HTML boilerplate for you.<br>
Create an `h1` element within your `body` element and give it the text `Nutrition Facts`.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Nutrition Label</title>
  </head>
  <body>
    <h1>Nutrition Facts</h1>
  </body>
</html>
```
> **Step 2** <br>
Below your `h1` element, add a `p` element with the text `8 servings per container`.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Nutrition Label</title>
  </head>
  <body>
    <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
  </body>
</html>
```
> **Step 3** <br>
Add a second `p` element with the text `Serving size 2/3 cup (55g)`.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Nutrition Label</title>
  </head>
  <body>
    <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
  </body>
</html>
```
> **Step 4** <br>
Within your `head` element, add a `link` element with the `rel` attribute set to `stylesheet` and the `href` attribute set to `https://fonts.googleapis.com/css?family=Open+Sans:400,700,800`.<br>
This will import the `Open Sans` font family, with the font weight values `400`, `700`, and `800`.<br>
Also add a `link` element to link your `styles.css` file.

```html
#index.html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8">
    <title>Nutrition Label</title>
    <link rel="stylesheet" href="styles.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css?family=Open+Sans:400,700,800">
  </head>
  <body>
    <h1>Nutrition Facts</h1>
    <p>8 servings per container</p>
    <p>Serving size 2/3 cup (55g)</p>
  </body>
</html>
```
> **Step 5** <br>
Create a `body` selector and give it a `font-family` set to `Open Sans` with a fallback of `sans-serif`.<br>
Remember that fonts with spaces in the name must be wrapped in quotes for CSS.

```css
#styles.css
body {
  font-family: 'Open Sans', sans-serif;
}
```
> **Step 6** <br>
The font is a bit small. Create an `html` selector and set the font to have a size of `16px`.

```css
#styles.css
html {
  font-size: 16px;
}
```
> **Step 7** <br>
Wrap your `h1` and `p` elements in a `div` element. Give that `div` a `class` attribute set to `label`.

```html
#index.html
  <body>
    <div class="label">
      <h1>Nutrition Facts</h1>
      <p>8 servings per container</p>
      <p>Serving size 2/3 cup (55g)</p>
    </div>
  </body>
```
> **Step 8** <br>
Borders can be used to group and prioritize content.<br>
Create a `.label` selector and give it a `border` set to `2px solid black`.

```css
#styles.css
.label {
  border: 2px solid black;
}
```
> **Step 9** <br>
Good use of white space can bring focus to the important elements of your page, and help guide your user's eyes through your text.<br>
Give your `.label` selector a `width` property set to `270px`.

```css
#styles.css
.label {
  border: 2px solid black;
  width: 270px;
}
```
> **Step 10** <br>
Give your `.label` selector a `margin` property set to `20px auto`, and a `padding` property set to `0 7px`.

```css
#styles.css
.label {
  border: 2px solid black;
  width: 270px;
  margin: 20px auto;
  padding: 0 7px;
}
```
> **Step 11** <br>
If you inspect your `.label` element with your browser's developer tools, you may notice that it's actually 288 pixels wide instead of 270. This is because, by default, the browser includes the border and padding when determining an element's size.<br>
To solve this, reset the box model by creating a `*` selector and giving it a `box-sizing` property of `border-box`.

```css
#styles.css
* {
  box-sizing: border-box;
}
```
> **Step 12** <br>
Remember that the use of `h1`, `h2`, and similar tags determine the semantic structure of your HTML. However, you can adjust the CSS of these elements to control the visual flow and hierarchy.<br>
Create an `h1` rule and set the `font-weight` property to `800`. This will make your `h1` text bolder.

```css
#styles.css
h1 {
  font-weight: 800;
}
```
> **Step 13** <br>
Give your `h1` selector a `text-align` property of `center`.

```css
#styles.css
h1 {
  font-weight: 800;
  text-align: center;
}
```
> **Step 14** <br>
Fine-tune the placement of your `h1` by giving it a top and bottom margin of `-4px` and a left and right margin of `0`.

```css
#styles.css
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
}
```
> **Step 15** <br>
Create a `p` selector and remove all margins.

```css
#styles.css
p {
    margin: 0;
}
```
> **Step 16** <br>
Lines can help separate and group important content, especially when space is limited.<br>
Create a `div` element below your `h1` element, and give it a `class` attribute set to `divider`.

```html
#index.html
    <div class="label">
      <h1>Nutrition Facts</h1>
      <div class="divider">
      </div>
      <p>8 servings per container</p>
      <p>Serving size 2/3 cup (55g)</p>
    </div>
```
> **Step 17** <br>
Create a selector for your new `.divider` and set the `border-bottom` property to `1px solid #888989`. Also give it a top and bottom margin of `2px`. It should not have any left or right margin.

```css
#styles.css
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
}
```
> **Step 18** <br>
The `letter-spacing` property can be used to adjust the space between each character of text in an element.<br>
Give your `h1` selector a `letter-spacing` property set to `0.15px` to space them out a bit more.

```css
#styles.css
h1 {
  font-weight: 800;
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}
```
> **Step 19** <br>
Nutrition labels have a lot of bold text to draw attention to important information. Rather than targeting each element that needs to be bold, it is more efficient to use a class to apply the bold styling to every element.<br>
Give your second `p` element a `class` attribute set to `bold`.

```html
#index.html
    <div class="label">
      <h1>Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size 2/3 cup (55g)</p>
    </div>
```
> **Step 20** <br>
Your new class does not have any styling yet. Create a `.bold` selector and give it a `font-weight` property set to `800` to make the text bold.<br>
Go ahead and remove the `font-weight` property from your `h1` selector as well.

```css
#styles.css
h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px;
}

.bold {
  font-weight: 800;
}
```
> **Step 21** <br>
Give your `h1` element a `class` attribute set to `bold`. This will make the text bold again.

```html
#index.html
    <div class="label">
      <h1 class="bold">Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size 2/3 cup (55g)</p>
    </div>
```
> **Step 22** <br>
Horizontal spacing between equally important elements can increase the readability of your text.<br>
Wrap the text `2/3 cup (55g)` in a `span` element, and give it a `class` attribute set to `right`.

```html
#index.html
    <div class="label">
      <h1 class="bold">Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size <span class="right">2/3 cup (55g)</span></p>
    </div>
```
> **Step 23** <br>
The `float` property is used to place an element on the left or right of its container, allowing other content (such as text) to wrap around it.<br>
Create a new `.right` selector and set the `float` property to `right`.

```css
#styles.css
.right {
  float: right;
}
```
> **Step 24** <br>
Wrap everything within the `.label` element in a new `header` element.

```html
#index.html
    <div class="label">
      <header>
      <h1 class="bold">Nutrition Facts</h1>
      <div class="divider"></div>
      <p>8 servings per container</p>
      <p class="bold">Serving size <span class="right">2/3 cup (55g)</span></p>
      </header>
    </div>
```
> **Step 25** <br>
Now update your `h1` selector to be `header h1` to specifically target your `h1` element within your new `header`.

```css
#styles.css
header h1 {
  text-align: center;
  margin: -4px 0;
  letter-spacing: 0.15px
}
```
> **Step 26** <br>
Create a new `div` element below your `header` element, and give it a `class` attribute set to `divider lg`.

```html
#index.html
      <div class="divider lg"></div>
```
> **Step 27** <br>
Create a new `.lg` selector and give it a `height` property set to `10px`. Also create an `.lg, .md` selector and set the `background-color` property to `black`.

```css
#styles.css
.lg {
  height: 10px;
}

.lg, .md {
  background-color: black;
}
```
> **Step 28** <br>
You may notice there is still a small border at the bottom of your `.lg` element. To reset this, give your `.lg, .md` selector a `border` property set to `0`.<br><br>
**Note:** the `md` (medium) class will be utilized in step 37 for the thinner bars of the nutrition label.

```css
#styles.css
.lg, .md {
  background-color: black;
  border: 0;
}
```
> **Step 29** <br>
Create a new `div` below your `.lg` element and give it a `class` attribute set to `calories-info`.

```html
#index.html
      <div class="calories-info"></div>
```
> **Step 30** <br>
Within your `.calories-info` element, create a `p` element. Give that `p` element a `class` attribute set to `bold sm-text`, and the text `Amount per serving`.

```html
#index.html
      <div class="calories-info">
        <p class="bold sm-text">Amount per serving</p>
      </div>
```
> **Step 31** <br>
The `rem` unit stands for `root em`, and is relative to the font size of the `html` element.<br>
Create an `.sm-text` selector and set the `font-size` to `0.85rem`, which would calculate to be roughly `13.6px` (remember that you set your `html` to have a `font-size` of `16px`).

```css
#styles.css
.sm-text {
  font-size: 0.85rem;
}
```
> **Step 32** <br>
Below your `.sm-text` element, create a new `h1` element with the text `Calories 230`. Wrap the `230` portion of the text in a `span` element with the `class` set to `right`.

```html
#index.html
      <div class="calories-info">
        <p class="bold sm-text">Amount per serving</p>
        <h1>Calories <span class="right">230</span></h1>
      </div>
```
> **Step 33** <br>
Create a new `.calories-info h1` selector setting the top and bottom margin to `-5px`, and the left and right margin to `-2px`.

```css
#styles.css
.calories-info h1 {
  margin: -5px -2px;
}
```
> **Step 34** <br>
Create a `.calories-info span` selector and set the `font-size` to `1.2em`.

```css
#styles.css
.calories-info span {
  font-size: 1.2em;
}
```
> **Step 35** <br>
The larger font size of the number `230` is causing it to overflow. Give the `.calories-info h1` an `overflow` property set to `hidden` to avoid this.

```css
#styles.css
.calories-info h1 {
  margin: -5px -2px;
  overflow: hidden;
}
```
> **Step 36** <br>
Typography is often more art than science. You may have to tweak things like alignment until it looks correct.<br>
Give your `.calories-info` span selector a `margin-top` set to `-7px`. This will shift your `230` text into place.

```css
#styles.css
.calories-info span {
  font-size: 1.2em;
  margin-top: -7px;
}
```
> **Step 37** <br>
Below your `.calories-info` element, add a `div` with the `class` attribute set to `divider md`.

```html
#index.html
      <div class="divider md">
      </div>
```
> **Step 38** <br>
Create an `.md` selector and give it a `height` property of `5px`.

```css
#styles.css
.md {
  height: 5px;
}
```
> **Step 39** <br>
Create a new `div` element below your `.md` element. Give it a `class` attribute set to `daily-value sm-text`. Within this new `div`, add a `p` element with the text `% Daily Value *`, and set the `class` attribute to `right bold`.

```html
#index.html
      <div class="daily-value sm-text">
        <p class="right bold">% Daily Value *</p>
      </div>
```
> **Step 40** <br>
The `float` styling is causing the new `p` element to be outside of the label's border. Use your existing `.divider` element as an example to add a new divider after the `p` element.

```html
#index.html
      <div class="daily-value sm-text">
        <p class="right bold">% Daily Value *</p>
        <div class="divider"></div>
      </div>
```
> **Step 41** <br>
Give the `.divider` selector a `clear` property set to `right`. This will clear the `float` property, pushing the divider and any following content down below the `float` text.

```css
#styles.css
.divider {
  border-bottom: 1px solid #888989;
  margin: 2px 0;
  clear: right;
}
```
> **Step 42** <br>
After your last `.divider` element, create a `p` element and give it the text `Total Fat 8g 10%`. Wrap `Total Fat` in a `span` element with the `class` set to `bold`. Wrap `10%` in another `span` element with the `class` set to `bold right`.

```html
#index.html
        <p><span class="bold">Total Fat</span> 8g <span class="bold right">10%</span></p>
```
> **Step 43** <br>
Below your element with the `Total Fat` text, create a new `p` element with the text `Saturated Fat 1g 5%`. Wrap the `5%` in a `span` with the `class` attribute set to `bold right`.

```html
#index.html
        <p>Saturated Fat 1g <span class="bold right">5%</span></p>
```
> **Step 44** <br>
This new `p` element will need to be indented. Give it a `class` set to `indent`.

```html
#index.html
        <p class="indent">Saturated Fat 1g <span class="bold right">5%</span></p>
```
> **Step 45** <br>
Create a new `.indent` selector and give it a `margin-left` property set to `1em`.

```css
#styles.css
.indent {
  margin-left: 1em;
}
```
> **Step 46** <br>
Create a `.daily-value p` selector to target all of your `p` elements in the `daily-value` section. Give this new selector a `border-bottom` set to `1px solid #888989`.

```css
#styles.css
.daily-value p {
  border-bottom: 1px solid #888989;
}
```
> **Step 47** <br>
The bottom borders under your `% Daily Value *` and `Saturated` `Fat 1g 5%` elements do not extend the full width of the label. Add `no-divider` to the `class` for these two elements.

```html
#index.html
      <div class="daily-value sm-text">
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
      </div>
```
> **Step 48** <br>
The `:not` pseudo-selector can be used to select all elements that do not match the given CSS rule.<br>
> ```css
> #styles.css
> div:not(#example) {
>   color: red;
> }
> ```
> The above selects all `div` elements without an `id` of `example`.<br>
> Modify your `.daily-value p` selector to exclude the `.no-divider` elements.

```css
#styles.css
.daily-value p:not(.no-divider) {
  border-bottom: 1px solid #888989;
}
```
> **Step 49** <br>
Now you will have to add separate dividers below your `.no-divider` elements.<br>
Your first `.no-divider` element has a `.divider` after it. Create another `.divider` after your second `.no-divider` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
```
> **Step 50** <br>
After your last `.divider`, create another `p` element with the text `Trans Fat 0g`. Italicize the word `Trans` by wrapping it in an `i` element. Give the new `p` element the `class` attribute set to `indent` `no-divider`.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
```
> **Step 51** <br>
Create another `.divider` after your last `p` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
```
> **Step 52** <br>
After your last `.divider`, create a new `p` element with the text `Cholesterol 0mg 0%`. Wrap the text `Cholesterol` in a `span` element, and give that `span` element the `class` attribute set to `bold`. Wrap the text `0%` in another `span` element, with the `class` set to `bold right`.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="bold right">0%</span></p>
```
> **Step 53** <br>
Below your last `p` element, create another `p` element with the text `Sodium 160mg 7%`. Wrap the text `Sodium` in a `span` element with a `class` attribute set to `bold`. Wrap the `7%` text in another `span` element with the `class` set to `bold right`.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="bold right">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="bold right">7%</span></p>
```
> **Step 54** <br>
Add another `p` element with the text `Total Carbohydrate 37g 13%`. Like before, use `span` elements to make the text `Total Carbohydrate` bold, and the text `13%` bold and right aligned.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
```
> **Step 55** <br>
Below your last `p` element, add another `p` element with the text `Dietary Fiber 4g`. Give the `p` element the `class` necessary to indent it and remove the dividing border. Then create a divider below that `p` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
```
> **Step 56** <br>
Create another `p` element after your last `.divider`, and give it the text `Total Sugars 12g`. Assign that `p` element the `class` values necessary to indent it and remove the bottom border. Then create another `.divider` below your new `p` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider"></div>
```
> **Step 57** <br>
The advantage to creating these dividers is that you can apply specific classes to style them individually. Add `dbl-indent` to the `class` for your last `.divider`.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="dbl-indent divider"></div>
```
> **Step 58** <br>
Create a `.dbl-indent` selector and give it a left margin of `2em`.

```css
#styles.css
.dbl-indent {
  margin: 2em;
}
```
> **Step 59** <br>
Below your `.dbl-indent` element, add a new `p` element with the text `Includes 10g Added Sugars 20%`. Your new `p` element should also be double indented, and have no bottom border. Use a `span` to make the `20%` bold and right aligned.<br>
Then create another divider after that `p` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider dbl-indent"></div>
        <p class="dbl-indent no-divider">Includes 10g Added Sugars <span class="bold right">20%</span></p>
        <div class="divider"></div>
```
> **Step 60** <br>
After your last divider, create another `p` element with the text `Protein 3g`. Use the necessary classes to remove the bottom border, and a `span` to make the `Protein` bold.<br>
Following this element, create a large divider.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider dbl-indent"></div>
        <p class="dbl-indent no-divider">Includes 10g Added Sugars <span class="bold right">20%</span></p>
        <div class="divider"></div>
        <p class="no-divider"><span class="bold">Protein</span> 3g</p>
        <div class="divider lg"></div>
```
> **Step 61** <br>
Create another `p` element below your large divider. Give the `p` element the text `Vitamin D 2mcg 10%`. Use a `span` to make the `10%` align to the right, but do not make it bold.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider dbl-indent"></div>
        <p class="dbl-indent no-divider">Includes 10g Added Sugars <span class="right bold">20%</span>
        <div class="divider"></div>
        <p class="no-divider"><span class="bold">Protein</span> 3g</p>
        <div class="divider lg"></div>
        <p>Vitamin D 2mcg <span class="right">10%</span></p>
```
> **Step 62** <br>
Create another `p` element, give it the text `Calcium 260mg 20%`. Align `20%` to the right. Below that, create a `p` element with the text `Iron 8mg 45%`, aligning the `45%` to the right.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider dbl-indent"></div>
        <p class="dbl-indent no-divider">Includes 10g Added Sugars <span class="right bold">20%</span>
        <div class="divider"></div>
        <p class="no-divider"><span class="bold">Protein</span> 3g</p>
        <div class="divider lg"></div>
        <p>Vitamin D 2mcg <span class="right">10%</span></p>
        <p>Calcium 260mg <span class="right">20%</span></p>
        <p>Iron 8mg <span class="right">45%</span></p>
```
> **Step 63** <br>
Create the final `p` element for your `.daily-value` section. Give it the text `Potassium 235mg 6%`. Align the `6%` text to the right, and remove the bottom border of the `p` element.

```html
#index.html
        <p class="right bold no-divider">% Daily Value *</p>
        <div class="divider"></div>
        <p><span class="bold">Total Fat</span> 8g<span class="bold right">10%</span></p>
        <p class="indent no-divider">Saturated Fat 1g <span class="bold right">5%</span></p>
        <div class="divider"></div>
        <p class="indent no-divider"><i>Trans</i> Fat 0g</p>
        <div class="divider"></div>
        <p><span class="bold">Cholesterol</span> 0mg <span class="right bold">0%</span></p>
        <p><span class="bold">Sodium</span> 160mg <span class="right bold">7%</span></p>
        <p><span class="bold">Total Carbohydrate</span> 37g <span class="right bold">13%</span></p>
        <p class="indent no-divider">Dietary Fiber 4g</p>
        <div class="divider"></div>
        <p class="indent no-divider">Total Sugars 12g</p>
        <div class="divider dbl-indent"></div>
        <p class="dbl-indent no-divider">Includes 10g Added Sugars <span class="right bold">20%</span>
        <div class="divider"></div>
        <p class="no-divider"><span class="bold">Protein</span> 3g</p>
        <div class="divider lg"></div>
        <p>Vitamin D 2mcg <span class="right">10%</span></p>
        <p>Calcium 260mg <span class="right">20%</span></p>
        <p>Iron 8mg <span class="right">45%</span></p>
        <p class="no-divider">Potassium 235mg <span class="right">6%</span></p>
```
> **Step 64** <br>
Add a medium divider after your `.daily-value` element. Below that new divider, create a `p` element with the `class` attribute set to `note`.<br>
Give the `p` element the following text:<br><br>
> `* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.`

```html
#index.html
        <div class="divider md"></div>
        <p class="note">* The % Daily Value (DV) tells you how much a nutrient in a serving of food contributes to a daily diet. 2,000 calories a day is used for general nutrition advice.</p>
```
> **Step 65** <br>
Create a `.note` selector, and set the size of the font to `0.6rem`. Also set the top and bottom margins to `5px`, removing the left and right margins.

```css
#styles.css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
}
```
> **Step 66** <br>
Give the `.note` selector a left and right padding of `8px`, removing the top and bottom padding. Also set the `text-indent` property to `-8px`.<br><br>
With these last changes, your nutrition label is complete!

```css
#styles.css
.note {
  font-size: 0.6rem;
  margin: 5px 0;
  padding: 0 8px;
  text-indent: -8px;
}
```