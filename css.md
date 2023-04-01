CSS Background
--------------

background-color  -> red/rgb(255,0,0)/#ff0000/transparent;
background-image -> url('paper.gif') 	
background-repeat: repeat/repeat-x/repeat-y/no-repeat;
	By default, the background-image property repeats an image both horizontally and vertically.
background-attachment -> scroll/fixed/inherit
background-position -> top right -> position of the image in the background
	top,left,center,bottom, xpos ypos,x% y%

background:#ffffff url('img_tree.png') no-repeat top right -> Shortcut

Order of Shortcut:
    * background-color
    * background-image
    * background-repeat
    * background-attachment
    * background-position


CSS Text
--------
For W3C compliant CSS: If you define the color property, you must also define the background-color property. 
1) color:red/rgb(255,0,0)/#ff0000;
2) text-align: center/left/right/justify;
	text-align is set to "justify", each line is stretched so that every line has equal width, and the left and right margins are straight.
3) text-decoration:overline/line-through/underline/blink/none
	mostly used to remove underlines from links for design purposes
4) text-transform: uppercase/lowercase/capitalize;
5) text-indent: 10px;
	indentation of the first line of a text
6) letter-spacing: +ve and -ve
7) line-height: space between lines
8) direction:rtl ->right to left
9) word-spacing: 
10) white-space: nowrap/pre; [the text is not wrapped at all]
11) vertical-align: baseline/ sub/ super/ top/ text-top/ middle/ bottom/ text-bottom/ 
	alignment of text along with images 
12) text-shadow: none/color/length


CSS Font
--------
Generic families:
	serif -> Times New Roman, Georgia
	sans-serif -> Arial, Verdana -> No lines on the tip of characters
	Monospace -> Courier New, Lucida Console -> All characters of same width
Name of a font family is more than one word, it must be in quotation marks, like font-family: "Times New Roman"	

SAFE FONTS: http://www.w3schools.com/Css/css_websafe_fonts.asp

1) font-family:"Times New Roman", Times, serif
2) font-style: normal/italic/oblique
3) font-size: 
	If you do not specify a font size, the default size for normal text, like paragraphs, is 16px (16px=1em).
	em size unit is recommended by the W3C.
	
	xx-small/ x-small/ small/ medium/ large/ x-large/ xx-large/ smaller/ larger/

	The solution that works in all browsers, is to set a default font-size in percent for the body element:
	body {font-size:100%}
	h1 {font-size:2.5em}
4) font-variant: normal/small-caps
5) font-weight: normal/bold/bolder/lighter/100;

Shortcut: font:italic bold 12px/30px Georgia, serif;
 	  <font-style> <font-variant> <font-weight> <font-size>/<line-height> <font-family>
 	  
 	  
CSS Links
---------

a:link - a normal, unvisited link
a:visited - a link the user has visited
a:hover - a link when the user mouses over it
a:active - a link the moment it is clicked
	a:hover MUST come after a:link and a:visited
	a:active MUST come after a:hover

1) text-decoration
2) background-color
3) display
4) font-weight
5) color
6) width
7) text-align
8) padding   -> Normal Parameters of all items and Text


CSS Lists
---------

1) ul -> list-style-type: circle/square/disc/none
   ol -> list-style-type: armenian\ decimal\ decimal-leading-zero\ georgian\ lower-alpha\ lower-greek\ lower-latin\ lower-roman\ upper-alpha\ upper-latin\ upper-roman
   IE does not support ol list-style-type like greek etc.,
2) list-style-image: url('sqpurple.gif')
   IE and Opera will display the image-marker a little bit higher than Firefox, Chrome, and Safari.
   For cross-browser use background-image instead
   
   ul{
	   list-style-type: none;
	   padding: 0px;
	   margin: 0px;
   }
   li{
	   background-image: url(sqpurple.gif);
	   background-repeat: no-repeat;
	   background-position: 0px 5px;
	   padding-left: 14px;
   }
   
3) list-style-position: inside/outside; -> list-item markers should appear inside or outside the content flow   
   
4) Shorthand -> list-style: square url("sqpurple.gif");
   <list-style-type> <list-style-position> <list-style-image>


CSS Tables
----------

1) border: 1px solid black; 
	the table, th, and td elements have separate borders.To display a single border for the table, use the border-collapse property.
2) border-collapse:collapse;
	If a !DOCTYPE is not specified, the border-collapse property can produce unexpected results.
3) width: 100px / 100%
4) text-align:right/left/center -> sets the horizontal alignment
5) vertical-align: top, bottom, or middle
6) padding: 10px; spacing between border and the content inside -> can be set for table and td
	can be used in top right bottom left combination
7) background-color:green;
8) color:white;
9) caption-side: top/bottom/left/right -> placement of caption


CSS Box Model
-------------

margins, borders, padding, and the actual content.
   _________________________
 | MARGIN		    |
 |  _____________________   |
 | |BORDER		|   |
 | |  _______________   |   |
 | |  |	PADDING      |	|   |
 | |  |	 ________    |  |   |
 | |  |	|CONTENT|    |	|   |
 | |  | --------     |	|   |
 | |  |______________|	|   |
 | |   		        |   |
 | ----------------------   |
 |--------------------------
 
 
 Margin - Clears an area around the border. The margin does not have a background color, and it is completely transparent
 Border - A border that lies around the padding and content. The border is affected by the background color of the box
 Padding - Clears an area around the content. The padding is affected by the background color of the box
 Content - The content of the box, where text and images appear
 
 IE includes padding and border in the width, when the width property is set, unless a DOCTYPE is declared.
 
 
 CSS Border
 ----------
 Shorthands: 
 border: <border-width> <border-style> <border-color>
 border-bottom : -do-
 border-left: -do-
 border-right: -do- 
 border-top: -do-
     To set the borders invidually
     
border-color: color_name/hex_number/rgb_number/transparent  -> can be used as border-left-color

border-color:#ff0000 #00ff00 #0000ff rgb(250,0,255); -> for setting top to left combo
	The "border-color" property does not work if it is used alone. Use the "border-style" property to set the borders first.
	
border-style: none\hidden\dotted\dashed\solid\double\groove\ridge\inset\outset\inherit\ -> can be used as border-left-style

border-width: thin/medium/thick/length -> can be used as border-left-width


color,style and width follows the combo structure from top to left


CSS Outlines
------------
Shorthand -> outline: <outline-color> <outline-style> <outline-width>

outline-color: color_name/hex_number/rgb_number/invert
outline-style: none/dotted/dashed/solid/double/groove/ridge/inset/outset
outline-width: thin/medium/thick/length

	Internet Explorer 8 (and higher) supports the outline properties if a !DOCTYPE is specified.


CSS Margins
-----------

margin: auto/length/%
	The browser sets the margin. The result of this is dependant of the browser

margin-top:100px;
margin-bottom:100px;
margin-right:50px;
margin-left:50px;

Shorthands

margin:25px 50px 75px 100px;

    * top margin is 25px
    * right margin is 50px
    * bottom margin is 75px
    * left margin is 100px

margin:25px 50px 75px;

    * top margin is 25px
    * right and left margins are 50px
    * bottom margin is 75px

margin:25px 50px;

    * top and bottom margins are 25px
    * right and left margins are 50px


CSS Padding
-----------

padding is inside the border

works same as padding including the shorthand formats

padding-top:25px;
padding-bottom:25px;
padding-right:50px;
padding-left:50px;




CSS Grouping and Nesting Selectors
----------------------------------
To minimize the code, you can group selectors.Separate each selector with a comma.
h1,h2,p {
 color:green;
}


It is possible to apply a style for a selector within a selector.

p{
  color:blue;
  text-align:center;
}
.marked {
  background-color:blue;
}
.marked p{
  color:white;
}



CSS Dimension
-------------
max-width and min-width takes precedence over width and similarly max-height, min-height takes precedence over height


CSS Display and Visibility
--------------------------
visibility:hidden hides an element, but it will still take up the same space as before.
display:none hides an element, and it will not take up any space.


A block element is an element that takes up the full width available, and has a line break before and after it.
    <h1>, <p>, <div>
    
An inline element only takes up as much width as necessary, and does not force line breaks.
    <span> <a>
    

An inline element set to display:block is not allowed to have a block element nested inside of it.    



display: none/inline/block/list-item/run-in/compact/marker/table/inline-table/table-row-group/table-header-group/table-footer-group/table-row/table-column-group/table-column/table-cell/table-caption
visible: hidden/visible/collapse
        collapse -> collapses to the nearest table row, similar to border-collapse
        
	Internet Explorer does not support the value "collapse".


CSS Positioning
---------------

Elements can be positioned using the top, bottom, left, and right properties. However, these properties will not work unless the position property is set first. 

An element with fixed position is positioned relative to the browser window.
It will not move even if the window is scrolled:

position:fixed/relative/absolute/static

1) position:fixed;
Internet Explorer supports the fixed value only if a !DOCTYPE is specified.

position:relative;
left:-20px;
top:50px;

Even if the content of the relatively positioned element is moved, the reserved space for the element is still preserved in the normal flow.


position: absolute
An absolute position element is positioned relative to the first parent element that has a position other than static.


2) z-index:-1;
The z-index property specifies the stack order of an element (which element should be placed in front of, or behind, the others).

An element can have a positive or negative stack order:



3) top/bottom/right/left -> for positioning the element

4) clip:rect(0px,60px,200px,0px)  -> to display only that specific portion
   Can be used in icon images, which has classes assigned

5) cursor: url/auto/crosshair/default/pointer/move/e-resize/ne-resize/nw-resize/n-resize/se-resize/sw-resize/s-resize/w-resize/text/wait/help/

6) overflow: auto/ hidden/ scroll/ visible/ inherit


CSS Float
---------

With CSS float, an element can be pushed to the left or right, allowing other elements to wrap around it.
Float is very often used for images, but it is also useful when working with layouts.

Elements are floated horizontally, this means that an element can only be floated left or right, not up or down.

A floated element will move as far to the left or right as it can. Usually this means all the way to the left or right of the containing element.

The elements after the floating element will flow around it.

The elements before the floating element will not be affected.

If an image is floated to the right, a following text flows around it, to the left:

If you place several floating elements after each other, they will float next to each other if there is room.


clear: left/right/both/none
 	Specifies which sides of an element where other floating elements are not allowed


float: left/right/none 	


Simple Web page

div.container
{
	width:100%;
	margin:0px;
	border:1px solid gray;
	line-height:150%;
}
div.header,div.footer{
	padding:0.5em;
	color:white;
	background-color:gray;
	clear:left;
}
h1.header {
	padding:0;
	margin:0;
}
div.left
{
	float:left;
	width:160px;
	margin:0;
	padding:1em;
}
div.content
{
	margin-left:190px;
	border-left:1px solid gray;
	padding:1em;
}


1) First a container is placed for width:100%
2) Header div is placed. As div is not given any width expands to the full extent, same for footer
3) Div Left is used with a given width and Floated
4) Div Content is placed next to the LEFT Div Floated 




CSS Align
---------

Block elements can be aligned by setting the left and right margins to "auto".
	Using margin:auto will not work in Internet Explorer. See the next step in this tutorial for a crossbrowser fix.

Cross Browser Fix
.container{
	text-align:center;
}
.container .center{
	margin-left:auto;
	margin-right:auto;
	width:70%;
	background-color:#b0e0e6;
	text-align:left;
}



One method of aligning elements is to use absolute positioning:
.right{
position:absolute;
right:0px;
width:300px;
}


If a container element has a specified width, and the !DOCTYPE declaration is missing, IE will add a 17px margin on the right side. 
This seems to be space reserved for a scrollbar. 
Always set the !DOCTYPE declaration when using the POSITION and FLOAT property

it is always a good idea to predefine margin and padding for the <body> element. 

body {
	margin:0;
	padding:0;
}
.container{
	position:relative;
	width:100%
}
.right{
	position:absolute;
	right:0px;
	width:300px;
	background-color:#b0e0e6;
}

Float can also be used for alignment



CSS Pseudo Classes
------------------

Anchor:
a:link, a:visited, a:hover and a:active -> ALWAYS maintain this order for the CSS to be effective

:first-child pseudo-class matches a specified element that is the first child of another element. [Needs !DOCTYPE for IE]


p > i:first-child -> first i element in ALL P tags

The :lang pseudo-class allows you to define special rules for different languages. [IE8 and above if !DOCTYPE is given]

q:lang(no) {quotes: "~" "~"} -> quotation marks for q elements with lang="no"

:focus -> Adds a style to an element that has keyboard input focus



CSS Pseudo Elements
-------------------

:first-line -> to add a special style to the first line of a text
	    -> can only be used with block-level elements.
p:first-line{
  color:#ff0000;
}

Properties that can be used with :first-line are:
    * font properties
    * color properties 
    * background properties
    * word-spacing
    * letter-spacing
    * text-decoration
    * vertical-align
    * text-transform
    * line-height
    * clear
    
:first-letter -> to add a special style to the first letter of a text
	      -> can only be used with block-level elements.

Properties that can be used 
    * font properties
    * color properties 
    * background properties
    * margin properties
    * padding properties
    * border properties
    * text-decoration
    * vertical-align (only if "float" is "none")
    * text-transform
    * line-height
    * float
    * clear


:first-letter takes precedence over :first-line


:before -> used to insert some content before the content of an element. [IE8 and above if !DOCTYPE is given]
:after -> used to insert some content after the content of an element [IE8 and above if !DOCTYPE is given]



CSS Navigation Bars
-------------------
1) Create UL Items and Li Items 
ul {
   list-style-type:none;
   margin:0;
   padding:0;
}

2) Make the <a> as display:block to make the full line as clickable
3) a horizontal navigation bar. Using inline or floating list items.
4) Use Float for equal size Links [Use DOCTYPE for IE]
5) a{
  display:block;
  width:60px;
} 

Since block elements take up the full width available, they cannot float next to each other. We specify the width of the links to 60px



Image Opacity
-------------
A lower value makes the element more transparent.
In Firefox (opacity:x) x can be a value from 0.0 - 1.0. 
In IE (filter:alpha(opacity=x)) x can be a value from 0 - 100.

<img src="klematis.jpg" style="opacity:0.4;filter:alpha(opacity=40)"
onmouseover="this.style.opacity=1;this.filters.alpha.opacity=100"
onmouseout="this.style.opacity=0.4;this.filters.alpha.opacity=40" />

Text in Transparent Box

div.background{
  width:500px;
  height:250px;
  background:url(klematis.jpg) repeat;
  border:2px solid black;
  }
div.transbox{
  width:400px;
  height:180px;
  margin:30px 50px;
  background-color:#ffffff;
  border:1px solid black;
  /* for IE */
  filter:alpha(opacity=60);
  /* CSS3 standard */
  opacity:0.6;
  }
div.transbox p {
  margin:30px 40px;
  font-weight:bold;
  color:#000000;
  }


P tag will have the Text



Image Sprites
-------------

An image sprite is a collection of images put into a single image.

img.home {
	width:46px;
	height:44px;
	background:url(img_navsprites.gif) 0 0;
}

Specifies the Left and Top of the Image part needed


#home{left:0px;width:46px;}
#home{background:url('img_navsprites.gif') 0 0;}
   Positioned all the way to the left, and the width of the image is 46px


#prev{left:63px;width:43px;}
Positioned 63px to the right (#home width 46px + some extra space between items), and the width is 43px.
#prev{background:url('img_navsprites.gif') -47px 0;}
Defines the background image 47px to the right (#home width 46px + 1px line divider)

#next{left:129px;width:43px;}
Positioned 129px to the right (start of #prev is 63px + #prev width 43px + extra space), and the width is 43px.
#next{background:url('img_navsprites.gif') -91px 0;} 
Defines the background image 91px to the right (#home width 46px + 1px line divider + #prev width 43px + 1px line divider )	



CSS Media Types
---------------
@media rule allows different style rules for different media in the same style sheet

@media screen
  {
  p.test {font-family:verdana,sans-serif;font-size:14px}
  }
  
  
all  		Used for all media type devices
aural 		Used for speech and sound synthesizers
braille 	Used for braille tactile feedback devices
embossed 	Used for paged braille printers
handheld 	Used for small or handheld devices
print 		Used for printers
projection 	Used for projected presentations, like slides
screen 		Used for computer screens
tty 		Used for media using a fixed-pitch character grid, like teletypes and terminals
tv 		Used for television-type devices  



Attribute Selectors
-------------------

Internet Explorer 7 (and higher) supports attribute selectors only if a !DOCTYPE is specified.
Attribute selection is NOT supported in IE6 and lower.

[title] {
color:blue;
} 

-> styles all elements with a title attribute

[title=W3Schools] {
border:5px solid green;
} 

<h1 title="hello world">Hello world</h1>  -> [title~=hello] { color:blue; }

<p lang="en-us">Hi!</p> -> [lang|=en]{color:blue;}

input[type="text"] {width:150px;} -> can be used




CSS DONT's
----------
Avoid using the "behavior" attribute -> supported only by IE




Special chars cannot be used in property values except font-size
font:{large/150% sans-serif;}

multiple classes specific
.warning.urgent{background:silver} --> only elements with both warning and urgent class will have this

h1[class]{font-size:12px} --> attribute selectors
h1[class="urgent warning"] --> equals
h1[class~="urgent"] --> contains
h1[class|="urgent"] --> begins with
h1[class][id] --> both attributes

h1 + p{font-size:10px} --> selecting all P's which has h1 as a sibling just before it

pseudo class --> :link, :visited, :hover, :focus, :active

pseudo elements --> first-child, lang, first-letter, first-line

Generated Content 
	h2:before{content:"]]";color:silver;}
	h2:after{content:" The End";}

Order of Style Sheet definitions
	1) Reader important
	2) Author important
	3) Author normal
	4) Reader normal
	5) User agent declaration
	
	rgb(400%,500,-50%) --> is same as rgb(100%,255,0%)
	
	1 cm = 0.394 inches
	1 in = 2.54 cms = 25.4 mms
	1 in = 72 pts
		18pt = 0.25 in
		
	1pc = 12 pts
	1 in = 6pc
	
	In CSS, relative URLs are relative to the style sheet and NOT the HTML page
	
	h2{font: bold italic 200%/1.2 Verdana, Helvetica, Arial, sans-serif;}
	
	System Fonts: caption, icon, menu, message-box, small-caption, status-bar
	
	text-indent: length/percentage/inherit
	
	line-height: 1em; ---> inherits
	
	vertical-align: 
	
	text-decoration: underline overline
	
	white-space: normal, nowrap, pre, pre-wrap, pre-line
	
	display: inline-block --> If element width is not defined or auto, the element shrinks
	
	display:inline ---> width and text-align are ignored
	
	border: border-width border-style border-color
	
	border-top, border-bottom, border-right, border-left
	
	p{background-position: top right;}  -> places the image on top right of every paragraph
		if only one word, the other is center
	background-position: 0% 0% --> top left corner
						100% 100% --> bottom right corner
						20px 30px
						
	background-attachment: fixed/scroll
	
	background: color image repeat attachment position
	
	
	
	Inline element completely overlaps the floated image - background, border, content and all
	Block element have only their content appear on top of the float. Backgrounds and borders are placed behind the float
	
	min-width, min-height
	max-width, max-height
	
	overflow
	clip
	
	position: fixed absolute relative
	
	display: none inline block inline-block list-item run-in table
			 inline-table table-row-group table-header-group table-footer-group
			 table-row table-column-group table-column table-cell table-caption
			 
	border-collapse: collapse seperate
	
	border-spacing: 1px 2px vertical and horizontal
	
	empty-cells
	
	vertical-align: top middle bottom baseline...what is this?????  [For tables]
	
	
	
	Floating
---------

If an element is floated to the left, and another floated element is already there, the later element will be placed against the outer right edge of the previously floated element.

However, a floated element's top is below the bottom of all earlier floated images, then it can float all the way to the inner left edge of the parent.


Border-collapse
---------------

1) if one of the collapsing borders has border-style as hidden , it takes precedence over all others
2) If border-style none is present, it takes the lowest priority. Only if all the colliding borders have none, then
   the border will not be rendered. But the default value of border-style is none
3) If atleast one of the collapsing borders has a value other than none or hidden, then the narrow borders lose
   out to the wider ones. Most preferred to the least preferred: double, solid, dashed, dotted, ridge,outset,groove, inset
4) If color is different between borders: precedence is from : cell, row, rowgroup, column, column-group, table   
   
  

  
  
   O’Reilly’s CSS Pocket 
Reference 


ON WINDOWS
Andale Mono
Arial
Arial Black
Comic Sans
Courier New
Georgia
Impact
Times New Roman
Trebuchet MS
Verdana

ON MAC
Geneva
Courier
Helvetica
Times



font-size:   xx-small ,  x-small ,  small , medium ,  large ,  x-large , or  xx-large

Choose a keyword (we recommend small or medium) and specify it as the 
font size in your body rule.  This acts as the default size for your page.
Specify the font sizes of your other elements relative to your body font size 
using either em or percentages (the choice between em and percentages 
is yours, as they are essentially two ways to do the same thing).


Specify color by name
 background-color: rgb(80%, 40%, 0%);
 rgb(204, 102, 0);
 
 
 XHTML has an element we haven’t talked 
about called <del> that marks content in your XHTML as content that should be 
deleted. There is a similar element called 
<ins> that marks content that should be 
inserted. Typically browsers will style these 
elements with a strike-through and underline 
respectively


font-family: Verdana, Geneva, Arial, sans-serif
font-size: pix or em or %
	set body size as keyword[small or medium...] and make everything relative like em or %
color
font-weight
font-style
text-decoration



1) Simple Upgrades and colors
	body: font-size, font-family
	h1,h2: color
	h1: font-size
	h2: font-size
	
2) line-height in body - 1.6em
3) choose a paragraph and set
	border-color, border-width, border-style, background-color
4) line-height: 1.9em, color:#444444, font-family: Georgia, "Times New Roman", Times, serif
5) background-image, background-repeat, background-position: top left
6) The background-position property sets the position of the image and can be specified in pixels, or 
   as a percentage, or by using keywords like top, left, right, bottom, and center.
7) background-repeat: no-repeat, repeat-x, repeat-y, inherit

8) Instead of setting width, try setting the margin and the element sets its height itself
9) border-style: solid, double, groove, dotted, dashed, inset, outset, ridges
10) border-width:thin,medium,thick or in pixels
11) border-color: red, rgb(100%,0%,0%), #ff0000;
12) border-top-color, border-top-style, border-top-width and for bottom,left and right
13) text-align will align all inline content in a block element. 
14) the text inside the  <div> element is in nested block elements, but it is all aligned now.  That’s because these block 
    elements inherit the  text-align  property from the  <div> . So here’s the difference: rather than the  <div>  itself  aligning the 
    text in the headings and the paragraphs (which it won’t do because these are block elements), the headings and paragraphs 
    are inheriting the  text-align  value of  “center”, and then aligning their own content to center.
15)  line-height of  1em, or “1 times the font size of the elixirs element”, which in this case is “small”, or about 
     12 pixels (depending on your browser).  Remember, the elixirs  <div>  is inheriting its font-size from the  <body>  element, which we set to “small.”	
16)  line-height is a bit special because you can use just a number instead of  a relative measure – like em or % – for line-height.  
     When you use just a number, you’re telling each element in the elixirs  <div>  to have a line-height of  1 times its own font-size, rather than the font-size of the elixirs  <div> Pg:438 chap 10
	
17) padding, margin: top right bottom left
                   : top/bottom right/left

	border: thin solid #444444; --> works with any order and any number of elements
	
	background: color url repeat; white url(x.gif) repeat-x;
	
	font: font-style font-variant font-weight font-size/line-height font-family
	
	font-style font-variant and font-weight is optional
	
	  You can set the width of inline elements like <span>, <em> and <strong>, but you won’t notice any effect until you position them 
	  You can also add margin and padding to these elements, as well as a border.  
	  Margins and padding on inline elements work a little differently from block elements – if you add a margin on all sides 
	  of an inline element, you’ll only see space added to the left and right.  
	  You can add padding to the top and bottom of an inline element, but the padding doesn’t affect the spacing of the other inline elements around 
it, so the padding will overlap other inline elements.
Images are a little different from other inline elements.  The width, padding, and margin properties all behave more like they do for a block element

the right ordering is generally considered to be: link, visited, focus, hover, and then active.
0 0 0 
1 -> selectors have any id - one each
2 -> classes or pseudo-classes - one each
3 -> any element names - one each


IMPORTANT:
 When the browser places two block elements on top of  each othe) r, it collapses their shared margins together. The height of  the collapsed margin is the height of  the largest margin. 
 
  if the outer element has a border, the margins will never touch, so they won’t collapse. But if you remove the border, they will.
  
  Even when we set the width for a block element,  the paragraph is a block element, so no elements are going to move up beside it because all 
block elements have linebreaks before and after them.
  
  Making a float:
	1) Give it an identity
	2) Give it a width
	3) add float:right
	How:
		1) First the browser flows the elements on the page as usual, starting at the top of the file and moving towards the bottom.
		2)  When the browser encounters the floated element, it places it all the way to the right. It also removes the paragrap h from the flow, like 
			it’s floating on the page.
		3) Because the floated paragraph has been removed from the normal flow, the block elements are filled in, like the paragraph isn’t even there.
		4) The block elements are positioned under the floated element. That’s because the floated element is no longer part of the normal flow.
		5) But when the inline elements are positioned, they respect the boundaries of the floated element. So they are flowed around it
		6) However, when the inline elements are flowed within the block elements, they flow around the borders of the floating element.
	
	Any Div that needs to be floated is set first BEFORE the other elements that need to flow around it
	
	Steps:
		1) Give generoal settings like background-color, font and SET MARGIN to 0
		2) Next we have a rule for each logical section. In each, we’re tweaking the font size, adding padding and margins and also - in 
		   the case of main and the sidebar - specifying a background image.
		3) Next we set up the fonts and colors on the headings.
		4) And then some colors on the class called slogan, which is used in the sidebar <div>. And likewise with the beanheading class, which is used there as well.
		5) And for the last two rules in the Starbuzz CSS we use the a:link and a:visited pseudo-classes to style the links.
		6) Notice that we’re getting a nice dotted underline effect on the links by using a dotted bottom border instead of an underline. This is a great example of using 
		   the border property on an inline element. [text-decoration:none;border-bottom:thin dotted #ffffff;]
		   
For Floating:
1) Give the element you’re going to float a unique name using an  id .
2) Make sure the element’s XHTML is just below the element you want it to float under; in this case, the Starbuzz header.
3) Set a width on the element. 
4) Float the element to the left or the right.

So, what if we give the main content area a right margin that is at least as big as the sidebar? Then its content will extend almost to the sidebar, but not all the way.
Then we’ll have separation between the two, and since margins are transparent and don’t show the background image, the background color of the page itself should show through.

When you resize your browser to a wide position, the footer and the sidebar start to overlap.
The “main” <div> is short enough that the footer <div> is coming right up and overlapping with the sidebar <div>.

This happens because the sidebar has been pulled out of the flow. So, the browser just lays out the main and footer <div>s like it 
normally would, ignoring the sidebar (although remember that when the browser flows inline elements, it will respect the borders of the sidebar and wrap inline elements around it).

CSS clear  property: You can set this property on an element to request that as the element is being flowed onto the page, no floating content is allowed to be on the left, right, or both sides of  the element. 
#footer{clear:right;} because the sidebar is floated to the right

Now the footer is placed below the sidebar so that there are no floating elements to its right.

Unlike block elements that are flowed on the page, floated elements are just, well, floating.  In other words, the margins of floated 
elements aren’t actually touching the margins of the elements in the normal flow, so they can’t be collapsed. 

So you can easily end up having different margins on the sidebar and on the main content if you don’t remember that floated elements don’t collapse margins.

Jello Design:
1) Add a "All Content" Div to enclose all the Main DIVs
2) Set the width for it, to prevent the content from expanding on browser resize
3) To center the main "All content" Div, set the margin-left and margin-right as "auto"


Absolute Positioning:
1) position:absolute, top:100px, right: 200px, width:280px
2)  When an element is absolutely positioned, the first thing the browser does is remove it completely from the flow. 
	The browser then places the element in the position indicated by the  top  and  right  properties (you can use  bottom  and  left  as well).  
	In this case, the sidebar is going to be 100 pixels from the top of  the page, and 200 pixels from the right side of  the page. 
	We’re also setting a width on the  <div> , just like we did when it is floated
3) Elements that are in the flow don’t even wrap their inline content around an absolutely positioned element. 
4) The sidebar and annoyingad <div>s are layered on the page, with the annoyingad having a greater z-index than the sidebar, so it’s on top.   

position: 
	static[default]
	absolute
	fixed: places an element in a location that is relative to the browser window (rather than the page), so fixed elements never move
	relative: takes an element and flows it on the page just like normal, but then offsets it before displaying it on the page
	
Absolute Positioning for Sidebar:
	#sidebar{
		top:128px;
		right:0px;
		width:280px;
		position:absolute;
	}
	#main{
		margin-right:330px;
	}
	
If you’re positioning with respect to the <html> element, then the bottom property may not do what you’d expect. You’d think the “bottom” 
would be the very bottom of the Web page itself, but the <html> element actually defines this as the bottom of the browser window. So, 
if you want to absolutely position an element from the bottom of the page, rather than the browser window, you need to place your element inside an element 
that extends to the bottom of your page, and is positioned. One way to do this is to put your element into a relatively positioned element at the bottom of the page. 


Fixed positioning is always from the browser Window rather than the page
So, an element that stays even when scrolled we use FIXED positioning.

Internet Explorer version 6 (and earlier) doesn’t support fixed positioning

By specifying -90 pixels, we’re telling the browser to position the image 90 pixels to the left of the edge of the viewport.

Relative Positioning:  We can keep the element in the flow, have its space reserved, and then offset where it actually gets displayed.
Unlike absolute and fixed positioning, an element that is relatively positioned is still part of  the flow o f the page, but 
at the last moment, just before the element is displayed, the browser offsets its position

No matter how you tweaked the padding and margins you still can’t get an image to be positioned outside of  the box it’s in.

TAbles
-------

<table summary><caption>
table{
	caption-side:bottom
}
td, th {
    border: thin dotted gray;
}	

So instead of  a margin, we have a  border-spacing  property, which is defined over the entire table
IE version 6 doesn’t support border-spacing.
You can use a CSS property called border-collapse to collapse the borders so that there is no border spacing at all.

list-style-type: disc,square, circle, none

we can instead use the list-style-image: url ---> for defining the List Item Images

There’s a property called list-style-position. If you set this property to “inside” then your text will wrap under the marker. 
If you set it to “outside” then it will wrap just under the text above it.

XHTML also provides a  <fieldset>  element that can be used to group together common elements.  
<fieldset>  makes use of  a second element, called  <legend> . 

The <fieldset> element surrounds a set of input elements.
The <legend> provides a label for the group.

<frameset rows=”30%, *, 20%”>
   <frame name=”header” src=”header.html” />
   <frame name=”content” src=”content.html” />
   <frame name=”footer” src=”footer.html” />
</frameset>

<iframe name=”inlinecontent” src=”newcontent.html” width=”500” height=”200” />

<object classid=”clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B” 
        codebase=”http://www.apple.com/qtactivex/qtplugin.cab” 
        height=”200” 
        width=”300”>
   <param name=”src” value=”buckaroo.mov”>
   <param name=”autoplay” value=”true”>
   <param name=”controller” value=”true”>
   <embed height=”200” 
          width=”300” 
          src=”buckaroo.mov” 
          pluginspage=”http://www.apple.com/quicktime/download/” 
          type=”video/quicktime” 
          controller=”true” 
          autoplay=”true”>Sorry your browser does not support this movie type</embed>
</object>

Not to list the site for Search Indexing
<meta name=”robots” content=”noindex,nofollow” />













Special chars cannot be used in property values except font-size
font:{large/150% sans-serif;}

multiple classes specific
.warning.urgent{background:silver} --> only elements with both warning and urgent class will have this

h1[class]{font-size:12px} --> attribute selectors
h1[class="urgent warning"] --> equals
h1[class~="urgent"] --> contains
h1[class|="urgent"] --> begins with
h1[class][id] --> both attributes

h1 + p{font-size:10px} --> selecting all P's which has h1 as a sibling just before it

pseudo class --> :link, :visited, :hover, :focus, :active

pseudo elements --> first-child, lang, first-letter, first-line

Generated Content 
	h2:before{content:"]]";color:silver;}
	h2:after{content:" The End";}

Order of Style Sheet definitions
	1) Reader important
	2) Author important
	3) Author normal
	4) Reader normal
	5) User agent declaration
	
	rgb(400%,500,-50%) --> is same as rgb(100%,255,0%)
	
	1 cm = 0.394 inches
	1 in = 2.54 cms = 25.4 mms
	1 in = 72 pts
		18pt = 0.25 in
		
	1pc = 12 pts
	1 in = 6pc
	
	In CSS, relative URLs are relative to the style sheet and NOT the HTML page
	
	h2{font: bold italic 200%/1.2 Verdana, Helvetica, Arial, sans-serif;}
	
	System Fonts: caption, icon, menu, message-box, small-caption, status-bar
	
	text-indent: length/percentage/inherit
	
	line-height: 1em; ---> inherits
	
	vertical-align: 
	
	text-decoration: underline overline
	
	white-space: normal, nowrap, pre, pre-wrap, pre-line
	
	display: inline-block --> If element width is not defined or auto, the element shrinks
	
	display:inline ---> width and text-align are ignored
	
	border: border-width border-style border-color
	
	border-top, border-bottom, border-right, border-left
	
	p{background-position: top right;}  -> places the image on top right of every paragraph
		if only one word, the other is center
	background-position: 0% 0% --> top left corner
						100% 100% --> bottom right corner
						20px 30px
						
	background-attachment: fixed/scroll
	
	background: color image repeat attachment position
	
	
	
	Inline element completely overlaps the floated image - background, border, content and all
	Block element have only their content appear on top of the float. Backgrounds and borders are placed behind the float
	
	min-width, min-height
	max-width, max-height
	
	overflow
	clip
	
	position: fixed absolute relative
	
	display: none inline block inline-block list-item run-in table
			 inline-table table-row-group table-header-group table-footer-group
			 table-row table-column-group table-column table-cell table-caption
			 
	border-collapse: collapse seperate
	
	border-spacing: 1px 2px vertical and horizontal
	
	empty-cells
	
	vertical-align: top middle bottom baseline...what is this?????  [For tables]
	
	
	
	Floating
---------

If an element is floated to the left, and another floated element is already there, the later element will be placed against the outer right edge of the previously floated element.

However, a floated element's top is below the bottom of all earlier floated images, then it can float all the way to the inner left edge of the parent.


Border-collapse
---------------

1) if one of the collapsing borders has border-style as hidden , it takes precedence over all others
2) If border-style none is present, it takes the lowest priority. Only if all the colliding borders have none, then
   the border will not be rendered. But the default value of border-style is none
3) If atleast one of the collapsing borders has a value other than none or hidden, then the narrow borders lose
   out to the wider ones. Most preferred to the least preferred: double, solid, dashed, dotted, ridge,outset,groove, inset
4) If color is different between borders: precedence is from : cell, row, rowgroup, column, column-group, table   
   
  
  
	
		
	
 O’Reilly’s CSS Pocket 
Reference 


ON WINDOWS
Andale Mono
Arial
Arial Black
Comic Sans
Courier New
Georgia
Impact
Times New Roman
Trebuchet MS
Verdana

ON MAC
Geneva
Courier
Helvetica
Times



font-size:   xx-small ,  x-small ,  small , medium ,  large ,  x-large , or  xx-large

Choose a keyword (we recommend small or medium) and specify it as the 
font size in your body rule.  This acts as the default size for your page.
Specify the font sizes of your other elements relative to your body font size 
using either em or percentages (the choice between em and percentages 
is yours, as they are essentially two ways to do the same thing).


Specify color by name
 background-color: rgb(80%, 40%, 0%);
 rgb(204, 102, 0);
 
 
 XHTML has an element we haven’t talked 
about called <del> that marks content in your XHTML as content that should be 
deleted. There is a similar element called 
<ins> that marks content that should be 
inserted. Typically browsers will style these 
elements with a strike-through and underline 
respectively


font-family: Verdana, Geneva, Arial, sans-serif
font-size: pix or em or %
	set body size as keyword[small or medium...] and make everything relative like em or %
color
font-weight
font-style
text-decoration



1) Simple Upgrades and colors
	body: font-size, font-family
	h1,h2: color
	h1: font-size
	h2: font-size
	
2) line-height in body - 1.6em
3) choose a paragraph and set
	border-color, border-width, border-style, background-color
4) line-height: 1.9em, color:#444444, font-family: Georgia, "Times New Roman", Times, serif
5) background-image, background-repeat, background-position: top left
6) The background-position property sets the position of the image and can be specified in pixels, or 
   as a percentage, or by using keywords like top, left, right, bottom, and center.
7) background-repeat: no-repeat, repeat-x, repeat-y, inherit

8) Instead of setting width, try setting the margin and the element sets its height itself
9) border-style: solid, double, groove, dotted, dashed, inset, outset, ridges
10) border-width:thin,medium,thick or in pixels
11) border-color: red, rgb(100%,0%,0%), #ff0000;
12) border-top-color, border-top-style, border-top-width and for bottom,left and right
13) text-align will align all inline content in a block element. 
14) the text inside the  <div> element is in nested block elements, but it is all aligned now.  That’s because these block 
    elements inherit the  text-align  property from the  <div> . So here’s the difference: rather than the  <div>  itself  aligning the 
    text in the headings and the paragraphs (which it won’t do because these are block elements), the headings and paragraphs 
    are inheriting the  text-align  value of  “center”, and then aligning their own content to center.
15)  line-height of  1em, or “1 times the font size of the elixirs element”, which in this case is “small”, or about 
     12 pixels (depending on your browser).  Remember, the elixirs  <div>  is inheriting its font-size from the  <body>  element, which we set to “small.”	
16)  line-height is a bit special because you can use just a number instead of  a relative measure – like em or % – for line-height.  
     When you use just a number, you’re telling each element in the elixirs  <div>  to have a line-height of  1 times its own font-size, rather than the font-size of the elixirs  <div> Pg:438 chap 10
	
17) padding, margin: top right bottom left
                   : top/bottom right/left

	border: thin solid #444444; --> works with any order and any number of elements
	
	background: color url repeat; white url(x.gif) repeat-x;
	
	font: font-style font-variant font-weight font-size/line-height font-family
	
	font-style font-variant and font-weight is optional
	
	  You can set the width of inline elements like <span>, <em> and <strong>, but you won’t notice any effect until you position them 
	  You can also add margin and padding to these elements, as well as a border.  
	  Margins and padding on inline elements work a little differently from block elements – if you add a margin on all sides 
	  of an inline element, you’ll only see space added to the left and right.  
	  You can add padding to the top and bottom of an inline element, but the padding doesn’t affect the spacing of the other inline elements around 
it, so the padding will overlap other inline elements.
Images are a little different from other inline elements.  The width, padding, and margin properties all behave more like they do for a block element

the right ordering is generally considered to be: link, visited, focus, hover, and then active.
0 0 0 
1 -> selectors have any id - one each
2 -> classes or pseudo-classes - one each
3 -> any element names - one each


IMPORTANT:
 When the browser places two block elements on top of  each othe) r, it collapses their shared margins together. The height of  the collapsed margin is the height of  the largest margin. 
 
  if the outer element has a border, the margins will never touch, so they won’t collapse. But if you remove the border, they will.
  
  Even when we set the width for a block element,  the paragraph is a block element, so no elements are going to move up beside it because all 
block elements have linebreaks before and after them.
  
  Making a float:
	1) Give it an identity
	2) Give it a width
	3) add float:right
	How:
		1) First the browser flows the elements on the page as usual, starting at the top of the file and moving towards the bottom.
		2)  When the browser encounters the floated element, it places it all the way to the right. It also removes the paragrap h from the flow, like 
			it’s floating on the page.
		3) Because the floated paragraph has been removed from the normal flow, the block elements are filled in, like the paragraph isn’t even there.
		4) The block elements are positioned under the floated element. That’s because the floated element is no longer part of the normal flow.
		5) But when the inline elements are positioned, they respect the boundaries of the floated element. So they are flowed around it
		6) However, when the inline elements are flowed within the block elements, they flow around the borders of the floating element.
	
	Any Div that needs to be floated is set first BEFORE the other elements that need to flow around it
	
	Steps:
		1) Give generoal settings like background-color, font and SET MARGIN to 0
		2) Next we have a rule for each logical section. In each, we’re tweaking the font size, adding padding and margins and also - in 
		   the case of main and the sidebar - specifying a background image.
		3) Next we set up the fonts and colors on the headings.
		4) And then some colors on the class called slogan, which is used in the sidebar <div>. And likewise with the beanheading class, which is used there as well.
		5) And for the last two rules in the Starbuzz CSS we use the a:link and a:visited pseudo-classes to style the links.
		6) Notice that we’re getting a nice dotted underline effect on the links by using a dotted bottom border instead of an underline. This is a great example of using 
		   the border property on an inline element. [text-decoration:none;border-bottom:thin dotted #ffffff;]
		   
For Floating:
1) Give the element you’re going to float a unique name using an  id .
2) Make sure the element’s XHTML is just below the element you want it to float under; in this case, the Starbuzz header.
3) Set a width on the element. 
4) Float the element to the left or the right.

So, what if we give the main content area a right margin that is at least as big as the sidebar? Then its content will extend almost to the sidebar, but not all the way.
Then we’ll have separation between the two, and since margins are transparent and don’t show the background image, the background color of the page itself should show through.

When you resize your browser to a wide position, the footer and the sidebar start to overlap.
The “main” <div> is short enough that the footer <div> is coming right up and overlapping with the sidebar <div>.

This happens because the sidebar has been pulled out of the flow. So, the browser just lays out the main and footer <div>s like it 
normally would, ignoring the sidebar (although remember that when the browser flows inline elements, it will respect the borders of the sidebar and wrap inline elements around it).

CSS clear  property: You can set this property on an element to request that as the element is being flowed onto the page, no floating content is allowed to be on the left, right, or both sides of  the element. 
#footer{clear:right;} because the sidebar is floated to the right

Now the footer is placed below the sidebar so that there are no floating elements to its right.

Unlike block elements that are flowed on the page, floated elements are just, well, floating.  In other words, the margins of floated 
elements aren’t actually touching the margins of the elements in the normal flow, so they can’t be collapsed. 

So you can easily end up having different margins on the sidebar and on the main content if you don’t remember that floated elements don’t collapse margins.

Jello Design:
1) Add a "All Content" Div to enclose all the Main DIVs
2) Set the width for it, to prevent the content from expanding on browser resize
3) To center the main "All content" Div, set the margin-left and margin-right as "auto"


Absolute Positioning:
1) position:absolute, top:100px, right: 200px, width:280px
2)  When an element is absolutely positioned, the first thing the browser does is remove it completely from the flow. 
	The browser then places the element in the position indicated by the  top  and  right  properties (you can use  bottom  and  left  as well).  
	In this case, the sidebar is going to be 100 pixels from the top of  the page, and 200 pixels from the right side of  the page. 
	We’re also setting a width on the  <div> , just like we did when it is floated
3) Elements that are in the flow don’t even wrap their inline content around an absolutely positioned element. 
4) The sidebar and annoyingad <div>s are layered on the page, with the annoyingad having a greater z-index than the sidebar, so it’s on top.   

position: 
	static[default]
	absolute
	fixed: places an element in a location that is relative to the browser window (rather than the page), so fixed elements never move
	relative: takes an element and flows it on the page just like normal, but then offsets it before displaying it on the page
	
Absolute Positioning for Sidebar:
	#sidebar{
		top:128px;
		right:0px;
		width:280px;
		position:absolute;
	}
	#main{
		margin-right:330px;
	}
	
If you’re positioning with respect to the <html> element, then the bottom property may not do what you’d expect. You’d think the “bottom” 
would be the very bottom of the Web page itself, but the <html> element actually defines this as the bottom of the browser window. So, 
if you want to absolutely position an element from the bottom of the page, rather than the browser window, you need to place your element inside an element 
that extends to the bottom of your page, and is positioned. One way to do this is to put your element into a relatively positioned element at the bottom of the page. 


Fixed positioning is always from the browser Window rather than the page
So, an element that stays even when scrolled we use FIXED positioning.

Internet Explorer version 6 (and earlier) doesn’t support fixed positioning

By specifying -90 pixels, we’re telling the browser to position the image 90 pixels to the left of the edge of the viewport.

Relative Positioning:  We can keep the element in the flow, have its space reserved, and then offset where it actually gets displayed.
Unlike absolute and fixed positioning, an element that is relatively positioned is still part of  the flow o f the page, but 
at the last moment, just before the element is displayed, the browser offsets its position

No matter how you tweaked the padding and margins you still can’t get an image to be positioned outside of  the box it’s in.

TAbles
-------

<table summary><caption>
table{
	caption-side:bottom
}
td, th {
    border: thin dotted gray;
}	

So instead of  a margin, we have a  border-spacing  property, which is defined over the entire table
IE version 6 doesn’t support border-spacing.
You can use a CSS property called border-collapse to collapse the borders so that there is no border spacing at all.

list-style-type: disc,square, circle, none

we can instead use the list-style-image: url ---> for defining the List Item Images

There’s a property called list-style-position. If you set this property to “inside” then your text will wrap under the marker. 
If you set it to “outside” then it will wrap just under the text above it.

XHTML also provides a  <fieldset>  element that can be used to group together common elements.  
<fieldset>  makes use of  a second element, called  <legend> . 

The <fieldset> element surrounds a set of input elements.
The <legend> provides a label for the group.

<frameset rows=”30%, *, 20%”>
   <frame name=”header” src=”header.html” />
   <frame name=”content” src=”content.html” />
   <frame name=”footer” src=”footer.html” />
</frameset>

<iframe name=”inlinecontent” src=”newcontent.html” width=”500” height=”200” />

<object classid=”clsid:02BF25D5-8C17-4B23-BC80-D3488ABDDC6B” 
        codebase=”http://www.apple.com/qtactivex/qtplugin.cab” 
        height=”200” 
        width=”300”>
   <param name=”src” value=”buckaroo.mov”>
   <param name=”autoplay” value=”true”>
   <param name=”controller” value=”true”>
   <embed height=”200” 
          width=”300” 
          src=”buckaroo.mov” 
          pluginspage=”http://www.apple.com/quicktime/download/” 
          type=”video/quicktime” 
          controller=”true” 
          autoplay=”true”>Sorry your browser does not support this movie type</embed>
</object>

Not to list the site for Search Indexing
<meta name=”robots” content=”noindex,nofollow” />	
	
	


	
	
