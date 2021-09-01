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


        
 11. `width: calc((100% - 2 * #{$gutter-horizontal}) / 3);` and `width: calc((100% - 2* #{$gutter-horizontal}) / 3);`.
     in both of them only margin difference which is spanc between  2 and *. may be sass understand 2* as veriable. so give space.
 