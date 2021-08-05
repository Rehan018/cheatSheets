## Table of Contents :
- <b>[Mendatory Codes](#mendatory-codes)</b>
- <b>[Create Variable](#create-variable)</b>
- <b>[Background Image](#background-image)</b>
- <b>[Gradient Color](#gradient-color)</b>
- <b>[Text Formatting](#text-formatting)</b>
- <b>[Font Formatting](#font-formatting)</b>
- <b>[Text Shadow & Box Shadow](#text-shadow--box-shadow)</b>
- <b>[Flexbox](#flexbox)</b>
- <b>[Unselectable Text](#unselectable-text)</b>
- <b>[Hover to change Other Class Property](#hover-to-change-other-class-property)</b>
- <b>[Input Focus & Valid](#input-focus--valid)</b>
- <b>[Anchor Hover, Visited & Active](#anchor-hover-visited--active)</b>
- <b>[Animation](#animation)</b>
- <b>[Transition](#transition)</b>
- <b>[Scrollbar](#scrollbar)</b>
- <b>[CSS media for Responsive](#css-media-for-responsive)</b>

<hr />

### Mendatory codes
  
  ```
  *{
    margin: 0;
    padding: 0;
    box-sizing: border-box;
  }
  ::-webkit-scrollbar{
    display: none;
  }
  ```

### Create Variable
  
  ```
  :root{
    --color: #ddd;
    --bgcolor: #444;
  }
  body{
    background-color: var(--color);
    color: var(--bgcolor);
  }
  ```
  
### Background Image
  
  ```
  html{
    min-height: 100%;
    background-image: url(image.jpg);
    background-size: cover;
    background-repeat: no-repeat; repeat-x; repeat-y;
    background-position: center center; right top; left bottom;
    background-attachment: fixed; scroll;
  }
  ```
  
  <p align="center">OR</p>
  
  ```
  html{
    background: url(image.jpg) center center cover no-repeat fixed;
  }
  ```
  
### Gradient Color
  
  ```
  // background-image: linear-gradient(direction, color-stop1, color-stop2, ...)
  div{
    background-image: linear-gradient(to right, red, yellow);
    // OR
    background-image: linear-gradient(80deg, red, yellow);
    // OR Transparency
    background-image: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1));
  }
  ```
  
### Text Formatting
  
  ```
  text-transform: uppercase; lowercase; capitalize;
  text-indent: 50px;
  text-decoration: underline;
  text-decoration-color: #ddd;
  text-decoration-style: solid; wavy; double;
  text-shadow: 4px 4px 12px #aaa;
  text-overflow: ellipsis;
  text-align: justify;
  text-align-last: center; justify;
  line-height: 1em;
  vertical-align: middle; top; bottom;
  letter-spacing: 4px;
  word-spacing: 10px;
  direction: rtl; ltr;
  ```

### Font Formatting
  
  ```
  font-family: "Times New Roman", sans-serif;
  font-style: normal; italic; oblique;
  font-weight: normal; bold;
  font-variant: normal; small-caps;
  font-size: 1em;
  color: #444;
  ```
  
### Text Shadow & Box Shadow
  
  ```
  // text-shadow: horizontal vertical blur color;
  text-shadow: 2px 2px 8px #aaa;
  box-shadow: 2px 2px 8px #aaa, inset 0 2px 8px #bbb;
  ```
  
### FlexBox
  
  ```
  display: flex;
  flex-direction: column; row;
  flex-wrap: wrap; nowrap;
  justify-content: center;
  align-items: center;
  order: 3; 2;    // changing order
  flex-grow: 2; 3;    // changing width
  ```
  
### Unselectable Text
  
  ```
  -webkit-user-select: none;   /* Safari */        
  --moz-user-select: none;      /* Firefox */
  -ms-user-select: none;         /* IE10+/Edge */
  -user-select: none;                /* Standard */
  ```
  
### Hover to change Other CLass Property
  
  ```
  .class:hover + .hide{
    display: block;
  }
  .class:hover ~ .hide{
    display: block;
  }
  ```
  
### Input Focus & Valid
  
  ```
  input:focus, input:valid{
    // css codes
  }
  ```
  
### Anchor Hover, Visited & Active
  
  ```
  a:hover, a:visited, a:active{
    //  css codes
  }
  ```
  
### Animation
  
  ```
  animation: name 10s infinite reverse;
  
  @keyframes name{
    50%{  // css codes  }
  }
  ```
  
### Transform
  
  ```
  transform: translate(x, y); rotate(angle); rotateX(angle);
  ```
  
### Transition
  
  ```
  // transition: property duration timing;
  transition: all 5s;
  ```
  
### Scrollbar
  
  ```
  ::-webkit-scrollbar{
    width: 10px;
  }
  ::-webkit-scrollbar-track{
    background-color: #aaa;
  }
  ::-webkit-scrollbar-thumb{
    background-color: blue;
  }
  ::-webkit-scrollbar-thumb:hover{
    background-color: lightblue;
  }
  ```
  
### CSS media for Responsive
  
  ```
  // 1680 1280 980 740 480
  @media screen and (max-width: 1680px){
    //  css codes
  }
  ```
  
  
