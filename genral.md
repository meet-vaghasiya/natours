1. background-image:
    - if we want grediant or  overlay over image than we can pass both at once
        ```css
                background-image: linear-gradient(to right bottom, rgba(126, 213, 111, 0.8), rgba(40, 180, 133, 0.8)), url('/img/hero.jpg');
        ```
    - background-size and background-position often use with image:
        ```css
                background-size: cover;
                background-position: top; 
        ```

2.  clip-path:
     - this use for give shape to image like triangle , or any other plygon shape.
        ```css
            clip-path: polygon(0 0, 100% 0, 100% 75%, 0 100%);
        ```
3. remove default style
   - in **ul=>**    `list-style: none;` 
   - remove **underline and color from link=>**   `text-decoration: none;`
  
4. defualt setting:
    - by defualt box-sizing:border-box value is not inherited so put in body and tell in every elemet to inherti in `*` to **set** `box-sizing: inherit;` . also set `font-size: 62.5%;`
   
        ```
        *, *::before, *::after {
            margin: 0;
            padding: 0;
            box-sizing: inherit;
        }

        body {
        
            font-size: 62.5%;
            box-sizing: border-box;
        }
        ```

5. in conteainer or every row:
        ```
            .conateiner{
            max-width:112rem;
            margin:0 auto;
            }
        ```
            

6. for list items:

        ```css
        ul {
        list-style:none;
            &:not(:last-child) {
                margin-bottom: $list-vertical;
            }
        }

        ```
   
 


