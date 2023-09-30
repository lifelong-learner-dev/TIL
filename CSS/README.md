| | | ```<head> <link rel="stylesheet" href="1.css">``` | |
|:---:|:---|:---|:---|
| 1 | attributeSelector | input[type=""] {background: color;} <br> a[href=""] {color: color;} | type = "" <br> 1) text <br> 2) password  <br>   href^="value" /* start from value */  <br>  href$="value" /* end of value */  <br>  href*="value" /* includes value */ |
| 2 | box-shadow | providing shade to box |  |
| 3 | childSelector     | #header > h1 {color: color;}  <br>  #header > #nav > h2 {color: color;}  <br>  table th {color: color;} | ```Caution) The <tbody> element is included within the table's CSS``` |
| 4 | classSelector     | h3.cookTitle1 {}  <br>  .cookTitle2 {} | . = class|
| 5 | descSelector      | #header h1, h2 {color: color;} | #header should be attached to descendant |
| 6 | dynamicSelector   | div:hover {} <br> div:active{} | active : when it is clicked  selector: <br> 1) checked 2) focus 3) enabled 4)disabled |
| 7 | flexBox | /* flexible-box :  row direction  <br> (from left -> right)   <br> <br> column direction <br> (from top -> bottom)*/   <br><br>   !!! The parent box should be selected and defined first.  <br><br>   If 'display' is not set, the default value will be 'block'.   <br><br>  !!! display : flex   <br>  - default = block style <br><br> display : inline-flex  <br>  - default = inline-block style  <br><br>  display : block  <br>  - Lay out in rows  <br>  - Cannot be placed side by side <br> - With margin <br><br> display : inline  <br>  - Arranged side by side  <br>  - Takes up space only as much as the content,  without any margins  <br> - Even if width and height are set,<br> it doesn't apply display : inline-block <br> - Includes both inline and block characteristics  <br>  - Arranged side by side, with margins  <br><br> flex-direction: row;  <br>  - Flex item placement direction: horizontal direction.  <br><br>  flex-direction : column;  <br>  - Flex item placement direction: vertical direction.  <br><br>  **Item alignment method**  <br><br>  /* justify-content: space-between; //  <br>  Spacing added <br>- alignment according to the ratio. */  <br><br> /* justify-content: space-around; <br>// Spacing + space on both sides. */  <br><br>  /* justify-content: center; //  */  <br><br>  /* justify-content: space-evenly; /*  <br>  Center alignment with equal spacing.*/ <br><br>  /* justify-content: flex-end; */ | |
| 8 |idSelector | | # = id |
| 9 | inline-block | display: inline;  <br>  Width and height values are not applied  <br> <br>   float: right  <br>   Alignment to the right using inline and block elements. | |
| 10 | list | ul <br> li <br> { /*list-style-type: square;*/ <br> /*list-style-type: none; */ <br> display: inline;} <br> ul default value = type="disc" |  |
| 11 | mediaQuery | @media all and (min-width: 320px) { body {background-color: color;}} <br><br> @media all and (min-width: 768px) {body {background-color: color;}} <br><br> @media all and (min-width: 960px) {body {background-color: color;}} <br><br> Vertical) orientation:portrait  Horizontal) orientation:landscape <br><br> @media all and (orientation: portrait) {body {background-color: color;}} <br><br> @media all and (orientation: landscape) {body {background-color: color;}} <br><br> * {margin: 0; padding: 0;} <br><br> /* same as = body {margin:0; padding:0;} */ | To provide a flexible design based on screen size. |
| 12 | first-child | #content div:first-child <br> {background-color: color;} <br><br> #content div:first-child + div + div <br> {background-color: color;} | first-child + div + div : it goes deeper  |
| 13 | nth-child | #content div:nth-child(2) <br> {background-color: color;} <br><br> #content div:nth-child(4) <br> {background-color: color;} <br><br> table <br> {margin: 0 auto; border-collapse: collapse; <br><br> /*single borderline*/ } | nth-child(2) : 2nd child nth-child(7) : 7th child |
| 14 | overflow | /* Hide content that overflows the specified parent div */<br><br> /* overflow: hidden; */<br><br>  /* Apply both horizontal and vertical scrolling */<br><br> /* overflow: scroll; */ <br><br> /* Apply automatic scrolling */ <br><br>   overflow: auto; | |
| 15 | position | #boxB {position: relative;} <br><br> #parent {position: absolute;} <br><br> #fixedBox {position: fixed;} | (1) Apply relative positioning to boxB <br> /* relative: default value = static*/ <br><br> (2) Apply absolute positioning to boxB <br>/* Because the positioning was not specified relative to the parent element,<br> it is based on the browser viewport (body)*/ <br><br> (3) Position boxB inside the parent element <br> Set position to relative on the parent <br>(results are the same when set to absolute,<br> with slight differences)*/<br><br> boxB is positioned as      absolute <br> /* Difference between absolute and relative         positioning in the parent context */ <br> /* - Difference in the document's default margins! */ |
| 16 | stateSelector |  ```/*White when <input> tag is usable``` <br> ```and inputtable */```<br><br> ```input:enabled {background-color: white;}``` <br><br>  ```/*Entered sky blue when the <input> tag is unavailable.*/``` <br><br> ```input:disabled {background-color: skyblue;}``` <br><br>  ```/* <When <input> tag receives focus, input field becomes orange */``` <br><br> ```input:focus {background-color: orange;}``` | |
| 17 | tagSelector | h3 <br> {background-color: #000000; <br> color: #fff; <br> width: 50%; <br> margin-left: 20px;} | |
| 18 | varFont | .vw {font-size: 5vw;} <br><br>  .vh {font-size: 5vh;} <br><br> .vmin {font-size: 5vmin;} <br><br> .vmax {font-size: 5vmax;} | ```<body>``` <br> ```<p class="vw">vw </p>``` <br> ```<p class="vh">vh</p>``` <br> ```<p class="vmin">vmin</p>```<br> ```<p class="vmax">vmax</p>``` <br> ```</body>``` |
| 19 | varMargin | #wrap <br> {margin: 0 auto;<br> width: 90%;<br> height: 300px;<br> border: 4px solid black;}<br><br>  #wrap div <br>{display: inline-block;<br> height: 100%;}<br><br>  #wrap div:nth-child(1)<br> {width: 33.3%;<br> background-color: green;}<br><br>  #wrap div:nth-child(2)<br> {width: 66.7%;<br> background-color: yellow;} | <body>     <div id="wrap">       <div></div>       <div></div>     </div> </body> |
| 20 | visibility | /* Semi-transparent when hovered with the mouse */<br><br> #f1:hover {opacity: 0.5;}<br><br>  /* Fully opaque when clicked with the mouse */<br><br> #f1:active {opacity: 1;}<br><br>  /* Hidden when clicked with the mouse */<br><br> #f2:active <br>{visibility: hidden; } | |
| 21 | z-index | #outBox <br>{position: relative;<br> margin: 0 auto;<br> width: 1020px;}<br><br>  #box1 <br>{position: absolute;<br> left: 25px;<br> top: 181px;<br> z-index: 1;}<br><br>  #box2 <br>{position: absolute;<br> left: 187px;<br> top: 155px;<br> z-index: 2;}<br><br> #box3 <br>{position: absolute;<br> left: 369px;<br> top: 129px;<br> z-index: 5;}<br><br> #box4 {position: absolute;<br> left: 603px;<br> top: 155px;<br> z-index: 4;}<br><br> #box5 <br>{position: absolute;<br> left: 795px;<br> top: 181px;<br> z-index: 3;} | |
| 22 | float | | |
| 23 | padding | padding: Inner spacing within the area <br>(indentation effect).| |
| 24 | margin | margin: External spacing <br> (spacing effect between other elements). | |
| 25 | a:hover | ul<br> li<br> a:hover<br> img:hover | hover: When the mouse is placed over it.<br><br> ul <br> li : table |
| 26 | font  | font-family: priority of font-style <br><br> font-size: 40px;<br> color: blue;<br> font-style: italic;<br> font-weight: bold; <br>text-decoration: underline;<br><br> letter-spacing: spacing between letters<br><br> word-spacing: spacing between words <br><br> line-height: line spacing <br><br> text-align: center;<br> text:shadow: 2px 2px 2px black <br>/*width height size color*/ | |
| 27 | border | border: solid 1px red;<br> border-style: solid;<br> border-width: 3px;<br><br> /* thin medium thick */<br><br> border-left: dotted;<br> border-right: double;<br> border-bottom: dashed;<br> border-top: solid;<br> border-color: red;<br> border-radius: 10px;<br> /*make corners round*/<br><br> border-bottom-right-radius: 50px;| |
| 28 | float | Property that makes the element float.<br><br> In other words,<br> it means moving out of the default layout flow to the left or right.<br><br> left: Positioned to the left.<br><br> right: Positioned to the right. |  |
| | | ```</head>``` | | 