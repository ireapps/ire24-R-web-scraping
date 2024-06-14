# Web Scraping in R -- IRE2024
The basics of scraping web pages in R using rvest

### Basics of HTML structure
Get to know the structure of an HTML element - [https://developer.mozilla.org/en-US/docs/Glossary/Element](https://developer.mozilla.org/en-US/docs/Glossary/Element)
	
   - tags  `ex: <p> opens and </p> closes`
   - attributes `ex: id="shazam" inside the tag <p id="shazam">`
   - text `ex: <p>The text between opening and closing tags</p>`

A **table** built into HTML:\
![](https://github.com/ireapps/ire24-R-web-scraping/blob/main/images/html-table.png)


### Basic usage of functions in rvest

**Step 1**: read the html from a webpage into the RStudio environment using the `read_html()` function:\
\
ex. `html <- read_html("url")`

**Step 2**: pull a specific element from that html using `html_element()` or `html_elements()`:\
\
ex. `everything_inside_a_table_tag <- html_element("table")`\
ex. `everything_inside_a_p_tag <- html_element("p")`

**Step 3**: pull the text or contents from an html element using `html_text2()`:\
\
ex. `everything_inside_a_p_tag |> html_text2()`


### Websites we'll scrape in this class (we'll see how far we can get)

1 [https://www.dllr.state.md.us/employment/warn.shtml](https://www.dllr.state.md.us/employment/warn.shtml)

2 [https://dlr.sd.gov/workforce_services/businesses/warn_notices.aspx](https://dlr.sd.gov/workforce_services/businesses/warn_notices.aspx)

3 [https://www.billboard.com/charts/hot-100/](https://www.billboard.com/charts/hot-100/)

You'll find the finished scripts in the [finished_scripts](/finished_scripts) folder.