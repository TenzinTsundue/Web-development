# HTML
- header
- nav
- section
- main
- article
- aside
- footer
---
- figure
- figcaption
---
- video
- iframe
---
```
- <em></em> emphasize 
- <mark></mark> highlight
- <q></q> quotation 
```
--
```
- <blockquote></blockquote>
- <code></code>
- <pre></pre> preformatting
```
---
- table
- thead
- tbody
- colgroup
- col
---

# CSS

### **Class** : represent by "."
```
.blue-text {
    color: blue;
}

<p class = "blue-text"> lorem </p>

// Can have multiple classes with a space in between

<p class = "blue-text centerclass"> lorem </p>
```
### import google fonts
```
<link href="heregoesthelink" rel = "stylesheet" type = "text/css">

h2 {
    font-family: font name, 2ndoption;
}
```
### **ID** : represent by "#"
// higher priority to id then classes
```
#heading {
    color: green;
}

<form id = "heading">Content</form>
```
Margin
Border
padding (top-right-bottom-left in order)
```
padding: 40px 20px 20px 40px;   //clockwise notation
```
### Attribute selectors
```
<style>
    [type = 'radio'] {
        margin: 20px
    }
</style>

### em and rem (relative value)

em = font (relative to parent font size)

### Importent

.pink-text {
    color: pink !important;
}
```
### Hexcolor and rgb color
```
color: #000000;
color: #F00;

color: rgb(255,255,255);
```
### **CSS variable** represented by "--" 
```
.penguin {
    --penguin-skin: black;
    --penguin-belly: gray;
}

.penguin-top {
    background: var(--penguin-skin, gray); //gray as a fall back value
}
```
### cascading CSS variables
//variable in root can be used throughout the page
```
<style>
    :root {
        --penguin-belly: pink;
    }
</style>
```
## CSS grid
```
.container {
    display: grid;
    grid-template-columns: 100px 100px 100px;
    gird-template-rows: 50px 50px;
    grid-gap: 10px 20px;
}
// grid-template-columns: auto 50px 10% 2fr 1fr;   //fr for fraction

<div class= "container">
    <div class= "d1">1</div>
    <div class= "d1">2</div>
    <div class= "d1">3</div>
    <div class= "d1">4</div>
    <div class= "d1">5</div>
</div>
```
### grid control spacing
```
.item5 {
    grid-columns: 2/ 4;  #from 2 to 4
} 

### grid template

.container {
    grid-template-columns: 1fr 1fr 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-gap: 10px

    grid-template-areas:
    "header header header"
    "advert content content"
    "footer footer footer"
}

.item {
    grid-area: header;
    //grid-area: 1/1/2/4;   //same to the header
    //grid-area: 3/1/4/4;   //same to the footer
}
```
### repeat
```
 {
     grid-template-columns: repeat(3, 1fr);
     // grid-template-columns: 1fr 1fr 1fr;  //same
 }

//for respossive
 {
     grid-template-columns: repeat(auto-fill, minmax(60px, 1fr)); //autofill and minmax
     grid-template-columns: repeat(auto-fit, minmax(60px, 1fr)); 
 }
```
### media queries to create responsive layouts
```
.container {
    grid-template-areas:
    "header"
    "advert"
    "content"
    "footer";
}

@media (min-width: 300px) {
    .container {
        grid-template-columns: auto 1fr;
        grid-template-rows: auto 1fr auto;

        grid-template-areas:
        "advert header"
        "advert content"
        "advert footer";
    }
}
```
### Flexbox
```
//defalt flex dir is row
#box-container {
    height:500px;
    dispaly:flex;
    flex-direction: row-reverse;
}
```
# Bootstrap
>A CSS Framework

- General Default styles
    - Reboot: Set cross-browser style defaults
    - Tyypography: Default font family and size and weight
    - Tabels, images, figures: Default responsive styles
- Pre-define CSS Classes
    - 
- Grid Layout
    - container, rows and column
    - Row uses flexbox

CDN links
