1. difference between define in * and body
   -  IN `*` it's apply on all element. in `body` it's inherit element **inherit** from boody
    - that's why we we apply margin,padding,border-box in * and font-fize ,color,line height in body.
2. if you give letter spacing and centre element than element will not center correcly because it's also added specing after last char. so solve that add same amount of margin-right of negative number
   
    ```css
        letter-spacing: 50px;
        margin-right: -50px;
    ```

    -   also visit https://iamsteve.me/blog/remove-letter-spacing-from-last-letter

3. Give `button` or `a` element as **inline-block instad of block** .because it's take width according to content. 

| css propery       | block                     | inline-block                                                              |
| ----------------- | ------------------------- | ------------------------------------------------------------------------- |
| text-align:center | text inside button center | whole block center(trated as text and also width is according to content) |
| width             | 100%                      | width according to content                                                |  |  |


4. How z-index propery affect when trasform, and opacity ,please see this blog:
 -   https://www.freecodecamp.org/news/4-reasons-your-z-index-isnt-working-and-how-to-fix-it-coder-coder-6bc05f10
  
5. class and id of css should be based on `BEM` model.

6. sass folder strucher should be based on `7-1-pattern` modal. https://www.learnhowtoprogram.com/user-interfaces/building-layouts-preprocessors/7-1-sass-architecture

7. install node-sass in devDependecies because it's not require in product. at the end sass just convert into normal css. so use in devDependecies
    `npm i node-sass --save-dev`

8. other package like jqury use even in product so 
   `npm insall jquery --save`
      - thi will no loner required  after `npm 5.0+`  justo do `npm install jquery` 
      - event after npm 6.0+ just requried `npm i jquery`
      - verify above notes.
  
9. if you install npm packge globally thant it will not shown in `package.json`. so **may be affect in production.** so code is work in your machine and not in server or live. for example i have live serve install globally and not shown in package.json but still work.

10. first step of desing is always set the **max-width (use max-width  instead of width for responsive purpose)**
 of container.


        
 11. `width: calc((100% - 2 * #{$gutter-horizontal}) / 3);` and `width: calc((100% - 2* #{$gutter-horizontal}) / 3);`

     in both of them only margin difference which is spanc between  2 and *. may be sass understand 2* as veriable. so give space.


11. to give gradiant color to text
        ```css
        background-image: linear-gradient(to right, $color-primary-light, $color-primary-dark);
        display: inline-block;
        -webkit-background-clip: text;
        color: transparent;
        ```
12. we can also give text-shadow to the text.
    - `text-shadow: 0.5rem 1rem 2rem rgba($color-black, 0.2);`

13. `H1` element should be only **one time in whole page.** all other heading will be in `h2.` subheading will `h3,h4`

14. see compositins.scss file code for image scale up on hover and other image scall small.
15. if you want space in border than give outline propery in css.
        ```
                    outline-offset: 2rem;
                    outline: 1rem solid $color-primary;
        ```

16. font size 62.5% is not working same in html and body.please verify this.

17. below code (it's written in sass file) will select only all direct children.
        ```
        & > * {
                transform: skewY(7deg);
            }
        ```

18. backgrond-color: in linear-gradiant reutn invliad property valie in crome but in background-image give correct result. don't know why.. so always use background-image for grediant color.

19. if we use background-image and code in scss file url() file must be relative to the style.css file not your scss file . beacuse at the end code will return into css file. so if you give file from scss file than it will return  path from scss not from css.

20. `box-decoration-break` is use for beaak the word. if you use span and give padding than it will give only first and last . means suppose if word break due to specing and you reuiered specing in also new line . at this time it will reuqire.it's not work in google crome so use webkit prefix.  
21. if you want to change outside content shape than use shape outside property in css use with webkit otherwise not work in mozilla browser.
22. if you skew div element. so all childs will also skew. so to skew in reverse direction use & > * {}. so back them in original position. if any child use transofrm already than it will not work so give them in them propery.
23. if you want to add caption in image than use figure propery and use img tag in that.

24.  if you see thin line while using transalate, animatinon and hover anywherer than give         `backface-visibility: hidden;` or         `overflow: hidden;` . 
25.  figcaption use for caption in image in figure element. if you want to show only in hover than use 
26.  for zoom out image first scale image and in hover use scale(1) .if you do first scale normal and than reduce scale(0.8) than image not fit in container and space is visible.  so always do first zoom image and than only scale to 1.
27.  for background video ,
     -   make write src in sorce inside video tag. 
     -   give loop, mutued, type attribute. 
     -   no need to wrap in content. give it's to absolte position. 
28.  `object-fit:cover` work same as `background-size:cover` . both  maintain aspect ration.
29.  we can pass mutiple artgument at diff stage in grediant color. and also give diff percenrage at diff color.
30. Lot's property is included in form.scss .please visit once.
**for input field**
    - color is not inhertied. so define color or use `color:inherit ` for same parent color
    -  font-family also not inherttied.
    - sudo class for input element: `:focus`,`:invalid`, `::-webkit-input-placeholder` ,`:placeholder-shown`.

32. use `visibility:hidden` and `opacity:0` , if you want animation .because animation is not work in `dispaly:none`.
33. 


