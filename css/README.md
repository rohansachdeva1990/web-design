# CSS Basics

## Showcase

#### Basic

1. [Implementing CSS](01_basic.html)
2. [Basic CSS Selectors](02_selectors.html)
3. [Fonts In CSS](03_fonts.html)
4. [Color Types](04_colors.html)
5. [Backgrounds & Borders](05_backgrounds_borders.html)
6. [Box Model, Margin & Padding](06_box_model.html)
7. [Float & Alignment](07_float_align.html)
8. [Link State & Button Styling](08_links_buttons.html)
9. [Navigation Menu Styling](09_menus.html)
10. [Inline, Block & Inline-Block Display](10_inline_block.html)
11. [Positioning](11_position.html)
12. [Form Styling](12_form_styling.html)
13. [Aside: Visibility, Order & Negative Margin](13_more.html)

#### Responsive Layouts

1. [Getting Started With Media Querie](./responsive-layout/01_media_queries.html)
2. [Em & Rem Units](./responsive-layout/02_em_rem.html)
3. [Vh & Vw Units](./responsive-layout/03_vh_vw.html)

#### Flexbox

1. [Flexbox Basics](./css-flexbox/01_flex_basics.html)
2. [Flexbox Properties](./css-flexbox/01_flex_properties.html)
3. [Flexbox Alignment](./css-flexbox/01_flex_align.html)

#### Advanced CSS

1. [Target Selectors](#)
2. [Nth-child Psuedo Selectors](#)
3. [before & after Psuedo Selectors](#)
4. [Box Shadows](#)
5. [Text Shadows](#)
6. [CSS Variables (Custom Properties)](#)
7. [Keyframe Animation 1](#)
8. [Keyframe Animation 2](#)
9. [CSS Transitions](#)
10. [Transform Property](#)

#### CSS Grid System

1. [Grid Basics & Columns](#)
2. [Grid Rows](#)
3. [Spanning Columns & Rows](#)
4. [Auto-Fit & Minmax](#)
5. [Grid Template Areas](#)
6. [Media Queries & The Grid](#)

## Notes & Recall

<details>
  <summary>Notes</summary>

#### Introduction

- CSS: Cascaded style sheets
- Cascading means the last effective style will be effective
- Link external CSS file by
  - `<link rel="stylesheet" href="style.css" type="text/css">`
- Internal CSS file, in the head section add `<style>`
- Inline using style attribute on the element
- In CSS always go from top to bottom, as we go down the css all the overridden will be given preference
- To add background to the website use background property in body tag
- User agent style sheet are style sheet provided by default for every html element by th browser
- To remove element from the DOM set display: none
- To hide an element, then set display: hidden

#### CSS Selectors

- Few important selector that we use in day to day. For reference check css-trick and w3schools - .class: can be applied to multiple elements
- #id: can be applied to single element
- \*: Means all elements
- element: eg h1, p etc
- element, element: h2, p {} → means apply same property to h2 and p
- element element: eg h2 p {..} → Means all p inside h2. It will apply only to p tags
- element.selector: You can combine the class selector with other selectors, like the type selector.
- element > element: eg h2 > p {} → Means all p that has parent h2
- element + element: h2 + p {} → means p element right after h2
- :hover:
- :last-child: eg h2 + p {} → means p element right after h2
- :first-child: similar as above
- !important (not recommended)
  - When we have conflicting property, and we don't want to allow it to be overridden, then we can use this property
- What selectors wins out in the cascade depends on:
  - Specifity
    - inline styles has the greatest
  - Importance
  - Source Order
    - When we have multiple style sheets imported in the same document. The one imported last in order will be given precedence

#### Text and Fonts

- Font should be a part of the "body' selector
- text-decoration: underline, line-through
- text-transform: uppercase
- line-height: Vertical space between lines
- font-style: italics, bold etc.
- font-weight
- font-size
- font-familty: font-family: "font1", "fallback-font2"...
- To make sure fonts are always available, try to use google fonts
- Standard font size to use: 16px
- Standard line-height: 1.6
- "justify" property spreads out the property when we reduce the size of screen

#### Units in CSS

- Absolute
  - cm: centimeters
  - mm: millimeter
  - in: inches
  - px: pixels (1px = 1/96 of an inch)
  - pt: points (1pt = 1/72 of an inch)
  - pc: picas (1pc = 12pt)
- Relative Units
  - %: related to parent element
  - em: related to font size of parent element
  - rem: related to font size of root element
  - vw: related to 1% of viewport width
  - vh: related to 1% of viewport height

#### Background, Border & Images

- Background

  - background-repeat: no-repeat
    - When you have small image as background, that image will repeat if no-repeat not set
  - background-position: X-axis Y-axis
    - center center
  - background-size: cover
    - Whole image will be shown
  - background syntax:-
    - background: url('path/to/image') no-repeat center center/cover
  - A "fixed" background, make the image fixed to the browser independent to scrolling

- Images

  - Jpg cannot be transparent
  - Png files can be transparent
  - Image tags are inline by default

- box-sizing: border-box; wraps the content inside the defined box type container.
  - makes sure that the elements inside the box does not increase the size of the box
- width vs max-width

  - width: When we reduce the size of the screen, after some point the scroll bar is visible
  - max-width: Auto resize when screen size is short

- Float
  - Try to work with "%" when using floats
  - Floats elements always needs to be cleared when moving on to next element
  - Float element is used to stack elements on the screen

#### Responive Layout
- max-width
- rem vs em
  - rem is preferred
- vh and vw units
  - View port is the whole area inside the browser, basically the browser body
  - 50vh means 50 of 100 view port height slices
  - each view port heioght is the slice across y to x axis moving downward
  - View port is always going to consist 100 of viewport height slices
    - No matter how big, tiny the browser screen is, there will always be 100 vh slices
  - vw is view port width, it is similar to vh but it goes across x axis towards right 
- check hotel website for responive transformation

#### Flexbox
- Modern layout mode in CSS3
- 'flex' is a value for the display property
- Replaces float and is much more elegant to work with
- Aligns item both horizontal(row) and vertical (column)
- Flex items can be re-ordered via CSS
- display: flex, creates a flex container
- All direct child elements within promotes to "flex items"
- All the child elment will be aligned horizontal by default.
- We can change direction fo flex accordingly
- Some important properties
  - justify-content: Align along with main axis (horizontal)
  - align-items: Align items along the cross axis (vertical)
  - align-content: Align when extra space in cross axis

</details>

<details>
  <summary>Review</summary>

- What is CSS?
- What do you mean by cascading?
- How to add multiple classes to an element?
- List important CSS selectors?
- Selectors priority depends on?
- How do you group selectors?
- What is the default value of the position property?
- Which property is used to change the font of an element?
- How do you group selectors?
- How to add vertical space between lines?
- What is 'float' property?
- Different ways to inclued CSS in your document?
- When to choose id and when to choose class?
- What is user agent style sheet?
- Where does the fonts goes in the website?
- Different between sans and sans-serif?
- What is the purpose of box-sizing?
- How to reset CSS?
- Difference between width and max-width?
- How to center a div?
- When to use 'important'?
- How to remove element from DOM?
- How to hide element?

</details>

## Tools, Tips & Tricks
- [Free Image Backgrounds](https://unsplash.com)
- [Color Hex](color-hex.com)
- [HTML Color Codes](htmlcolorcodes.com)
- [Color Paletton - With Color Scheme](https://paletton.com)
- [Learn CSS Selectors](https://flukeout.github.io/)
- [Specificity Calculator](https://specificity.keegan.st/)
- [Google Fonts](https://fonts.google.com/)
- [Quiz](https://www.w3schools.com/quiztest/quiztest.asp?qtest=CSS)


## References
- [CSS Tricks](https://css-tricks.com/)
- [MDN](https://developer.mozilla.org/en-US/docs/Web/CSS)

