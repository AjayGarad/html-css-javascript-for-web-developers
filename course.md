- HTML
    - Annotates content
    - Define document structure
    - browser will interpret the html page sequentially from top to bottom

- Why to write <!doctype html>:
    - this is historical
    - oldtime there were files which are not compliant to the standards
- help brower to render the content correctly brower usage doctype declaration to distinguish not compliant(render in quirks mode) and compliant pages(standard mode)

- content models
    - block level elements
    - inline elements
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

- h tag - `<h1></h1>, <h2></h2>, <h3></h3>, <h4></h4>, <h5></h5>, <h6></h6>`
    - specify heading - use for structuring of the code only

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
- li tag - `<li></li>`
    - all element in list are need in this tag
    - li can have ul tag
- ol tag - `<ol></ol>`
    - ordered list

- entity refrence
    - will help in rendering issue
    - if browser didnt understand the tag then it skip the data from it
    - we need to tell browser about difference between tag and tag as content by following ways
        - < - `&lt;`
        - > - `&gt;`
        - & - `&amp;`
        - copyright symbol - `&copy;`
        - space - `&nbsp;`
            - will use when we want some words to be always together instead breaking in new line
            - dont use to give more space in word instead use margin with span
        - " - `&quot;` - when charecterset is small instead utf-8 then it will cause issue with symbol