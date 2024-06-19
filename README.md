# Web Scraping in R -- IRE2024
The basics of scraping web pages in R using rvest

### Requirements for the class
-   [R and RStudio installed]()
-   tidyverse and rvest installed: `install.packages(c("tidyverse","rvest"))`
-   A browser with development tools (such as Chrome Inpsect)

### Basics of HTML structure
Get to know the structure of an HTML element - [https://developer.mozilla.org/en-US/docs/Glossary/Element](https://developer.mozilla.org/en-US/docs/Glossary/Element)
	
   - tags  `ex: <p> opens and </p> closes`
   - attributes `ex: id="shazam" inside the tag <p id="shazam">`
   - text `ex: <p>The text between opening and closing tags</p>`

A **table** built into HTML uses a **\<table>** tag. The **\<th>** tag is used for the header row; **\<tr>** for table row, **\<td>** for table data:
\
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

### Resources for help

-   check out Hadley Wickham's [tutorial on web scraping](https://www.r-bloggers.com/2020/04/tutorial-web-scraping-in-r-with-rvest/)
-   here's an [IRE tipsheet](https://docs.google.com/document/d/1Nd_X3Ee02xxMvKe0qwZWikD53ZSEL-x14nHihQEI-sk/edit?usp=sharing) on using browser development tools (such as Chrome Inspect)