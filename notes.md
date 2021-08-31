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


4.How z-index propery affect when trasform, and opacity ,please see this blog:
 -   https://www.freecodecamp.org/news/4-reasons-your-z-index-isnt-working-and-how-to-fix-it-coder-coder-6bc05f10
  
5.classi and id of css should be based on `BEM` model.

6. sass folder strucher should be based on `7-1-pattern` modal. https://www.learnhowtoprogram.com/user-interfaces/building-layouts-preprocessors/7-1-sass-architecture