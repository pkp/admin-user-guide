# Generate Reports - Examples and Tips

This section was originally authored by Andrea Kosavic at York University Library, and has been slightly revised \(mostly with OJS 3 updates\).

The Report Generator can be found in OJS 2 at Home &gt; User &gt; Journal Management &gt; Stats & Reports &gt; Generate Custom Report

The Report Generator can be found in OJS 3 at Dashboard &gt; Tools &gt; Statistics &gt; Generate Custom Report

## **A few tips for using the Report Generator**

* Note that the current day’s data will not be available until the next day
* The generator works like a funnel for data. The trick is to narrow down the bigger elements \(such as date range\), select what you’re interested in from there \(issues, articles, etc.\) then tweak the data at the end \(i.e. sort by number of downloads\).
* The Report Generator is most useful if you use the Advanced Options. All the examples below make use of the advanced options.
* The Report Generator spits out a URL at the very bottom that allows you to re-run your query at any time! Make sure to copy and save the URL somewhere so that you can re-run your search later \(it will disappear once the page is reloaded\).
* This section in the simple search... 

  ![](https://lh3.googleusercontent.com/zZgY3vgUHtOhTkLnfTsXOjWit7hn3dOkv14m0eCa7mz1oYb04KeV68mIJ4RC7TzDlA1l0nRrOQtyMr_VOzLlEDe0qEDqNtYweS9LgW5kbFeSJVskOJQGY6L7C1QMa617BTeXNkKi)

  ...is actually repeated in the “Columns” section below...along with a number of other options. \(Visible in the advanced options.\)  


  ![](https://lh4.googleusercontent.com/ZGkhfw8uSwd9Ovktc4GpTmHQIBnOg68tzRt6cBdLrelT3JMNrs4rskSw9Ezi4L_n42jeDRJ-WdpCgobnAamGH4fZUwrGU03wHCK2nd_-y6OGxJ1ihT8mfK2gLpYr1WcZ10uMLUNp)

## **Example report: How well has a particular \(i.e. most recent\) issue performed over the last few months?**

This particular query will give you a monthly count of how many full text galleys have been downloaded from a particular issue. You’ll have a column for month and total count for month, and a separate row for every month.

* Under “Default report templates” select “Article file downloads” from the dropdown list
* Uncheck all boxes in the “Aggregate stats by”
* Click on the “Month” radio button and enter date range under “Or select range by”

![](https://lh4.googleusercontent.com/x_CTGtrDYmxR_U5U9DQGu0RQ5JXxILPH7AJgmPwOag0Q7N5C2FEoWBlKcklp4Wdxm07NE7kxa3VzT6d3pg-kP3Bf5yKEpc9Jg-UBTz2BqKeOVIIe5X01Q-efifC518d7dEj9-qLZ)

* Select only “Month” under Columns

![](https://lh5.googleusercontent.com/UhAJbSjqNzSJpEOFoh0ySLvWbIOaJXUcr-3XMViX5d4Ul6iaHdjvM_WZvaPmFcK-4TjAhPIxVnzn76tD3lXCHn6UmdHKfO3ixLl54Th1W4ISE_e9yqFTxKCZvwMFLT7FeOwWOsjo)

* We want only a very light filtering of our data. Select the issue that you’re interested in, for example “Vol 6 \(2004\)” here. We also want to select only “Galley” under “By object type”

![](https://lh5.googleusercontent.com/yWzDH3FA568s_zjORIGNOmcbsaOqXy5qKUkWCVtUGrpveiENZxpYlnojJQlq4UJII9vRJ725NdsA0Ray0SNg9Ums50eKDEH8A3MFOdGCQ3TmM2WZuveridRbjzFRK-srsI4mi6zF)

* Ignore the “By geo location” and “Order by” options, and click “Generate custom report”
* You’ll end up with a very simple monthly report of the galley downloads for the one issue of interest for your journal.

![](https://lh3.googleusercontent.com/kJo1sgCOaiW1TzaSfEp-5QzE5J3tSizDUfenECMpOIK1LiCN5AV35tCiceFhUgXdv0JsgUUN25L9BfvRtt0TxyCIctLebk_KXtL76IelBE89YQtXq0wQ8LTydN6DnFgtCGuHjAZ8)

Save the URL at the bottom of the page for your records!

## **Example report: What are the most downloaded articles over the last 5 years?**

This report will present a list of article titles \(and the issues they come from\) ordered by descending download counts.

* Select “Article file downloads” from the dropdown box.
* Uncheck all boxes under “Aggregate stats by”
* Select the “Month” radio button and enter a date range

![](https://lh4.googleusercontent.com/x_CTGtrDYmxR_U5U9DQGu0RQ5JXxILPH7AJgmPwOag0Q7N5C2FEoWBlKcklp4Wdxm07NE7kxa3VzT6d3pg-kP3Bf5yKEpc9Jg-UBTz2BqKeOVIIe5X01Q-efifC518d7dEj9-qLZ)

