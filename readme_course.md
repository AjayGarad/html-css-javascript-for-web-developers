- HTML
    - Annotates content
    - Define document structure(structure of the content)
    - browser will interpret the html page sequentially from top to bottom
    - when origin precedence is in conflict then last declaration win cause html process sequentially top to bottom(same goes for css)
    - every element inherit the style property of parent element(document object model tree )

- Why to write <!doctype html>:
    - oldtime web pages were catagories in two format:
        - non compliant to the html standards(render in quirks mode)
        - compliant to html standard(render in standard mode)
    - So to help brower rendering content correctly doctype declaration is used

- [content model](https://www.w3.org/TR/2011/WD-html5-20110525/content-models.html)
    - block level elements
    - inline elements

- tags which can we use in HTML:
    - html tag
        - contain all the html document

    - head tag - `<head></head>`
        - main content of the page - auther desc, page title, external content, meta data
    - meta tag - `<meta>`
        - attribute - charset - to interpret content of the webpage
        _Eg._
        `<meta charset="UTF-8">`

    - title tag - `<title></title>`

    - body tag - `<body></body>`
        - contain all the content which need to show to user - also known as viewport

    - style tag - <style></style>
        - you can use style tag to define css for elements in same html file
    
    - link tag - <link>
        - rel attribute
            - will use to define type of attached document
        - href attribute
            - link path of the file
        - Eg.
        ```
        <link rel="stylesheet", href="style.css">
        ```
    - h tag - `<h1></h1>, <h2></h2>, <h3></h3>, <h4></h4>, <h5></h5>, <h6></h6>`
        - specify heading - use for structuring of the code only

    - style attribute - style=""
        - we can also define css style by using style attribute
    
    - class attibute - class=""
        - you can apply multiple class element by listing them like:
        ```
            <p class="name1 name2">
        ```
    - semantic element
        - dont give any new functionality than div tag or span tag
            - header tag - `<header></header>` (semantic element)

            - nav tag - `<nav></nav>` (semantic element)
                - mostly used for internal site navigation

            - section tag - `<section></section>` (semantic element)
            - article tag - `<article></article>` (semantic element)
            - aside tag - `<aside></aside>` (semantic element)
            - footer tag - `<footer></footer>` (semantic element)
    
    - unordered list tag - `<ul></ul>`
        - bulltin will come without number
    - li tag - `<li></li>`
        - all element in list are need in this tag
        - li can have ul tag
    - ordered list tag - `<ol></ol>`
        - bulletin will come with number

    - entity refrence
        - will help in rendering issue
        - if browser didnt understand the tag then it skip the data from it
        - we need to tell browser about difference between tag and tag as content by following ways
            - `< - &lt;`
            - `> - &gt;`
            - `& - &amp;`
            - `copyright symbol - &copy;`
            - `space - &nbsp;`
                - will use when we want some words to be always together instead breaking in new line
                - dont use to give more space in word instead use margin with span
            - `" - &quot;` - when charecterset is small instead utf-8 then it will cause issue with symbol

    - create link tag - <a></a>
        - attribute - href- hypertext refrence
            - value - #id or #name- will be used to jump on the same page with the tag have the same id or name
        - attribute - title - give info the web page reader about image
        - attribute - target - 
            - value - _blank - will open the link in new tab
    - image tag - <img></img>
        - attribute - src - path to image
        - attribute - width
        - attribute - height
        - browser will store the space for image if width and height attr are defined, if browser unable to load image data still web page will look proper according to lay out
        - attribute - alt - help screen reader

    - comment tag - <!-- code -->

- CSS - cascading styles sheet
    - css rule consist of selector(p) followed by open and close curly braces - inside it contain declartion - which contain property(color) and value(blue)
    - ex:
        p {color: blue;}
    - collection of css rules is call style sheet
    - cascading algorithm is used to combine property and value from different sources
    - origin merge inheritance specificity
    - selector type:
        - element selector
            ```
            p {
                color: blue;
                }
            ```
        - class selector 
            - use . before selector name
            ```
            .blue {
                color: blue;
                }
            ```
        - id selector
            - use # before selector name
            ```
            #name {
                color: blue;
                }
            ```
        - grouping selectors 
            ```
            div, .blue {
                color: blue;
                }
            ```
        - combining selectors
            - element with class selector
                ```
                p.big {
                    color: blue;
                    }
                ```
            - child selector
                - every p element which is direct child of an article element will apply the following style
                - not limited to element selector. we can use id, class, element
                ```
                article > p {
                    color: blue;
                }
                ```
            - descendent selector
                - every p element which are child of an article element will apply the following style
                - not limited to element selector. we can use id, class, element
                ``` 
                article p {
                    color: blue;
                }
                ```
            - adjuscent sibling selector
            - general sibling selector
        - pseudo selector
            - anyselector followed by : and then below pseudo selector
            - :link
            - :visited
            - :hover
            - :active
            - :nth_child(...)
                - value - number like 4 5, all odd level,all even level