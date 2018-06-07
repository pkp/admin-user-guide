# Generating reports

OJS’ reports can be broadly grouped into “usage” reports that contain usage metrics indicative of visitor readership, and “content” reports that provide data on the respective item \(eg. subscriber info\). Some of these reports also contain legacy information, provided that your OJS install was created at some point before OJS 2.4.3. OJS 3 has dropped support for legacy reports.  
****

The following table is a quick cheat sheet and comparison tool for each report; more detailed descriptions of each report follow.

### Comparison Table of All OJS Usage Reports

| Name | Description | Contents | Legacy | OJS 2 | OJS 3 |
| --- | --- | --- | --- | --- | --- |
| Timed Views | Provides article and galley views by date span. Can be used to retrieve legacy or current data. | Usage | Y/N | Y | N |
| View | Provides overall usage counts for abstract/landing page and galley downloads, per article. | Usage | Y | Y | N |
| Usage Statistics | Provides granular daily usage metrics for all article, article file, issue and homepage views/downloads. Will include visitor country data, if that is being logged. | Usage | N | Y | Y |
| Custom Report Generator | Customizable version of the Usage Statistics report, where various facets can be selected and specific date spans can be set. | Usage | N | Y | Y |
| COUNTER | Provides COUNTER reports for all journals on the OJS application. Provides monthly and year to date aggregate counts for abstract and galley views. | Usage | N | Y | Y |



### **Comparison Table of All OJS Content Reports**

| Articles | Provides general information on all articles in the system, incl. Title, abstract, authors, editor decision, and status. | Content | N | Y | Y |
| --- | --- | --- |
| Subscriptions | Provides information on any individual and institutional subscriptions. | Content | N | Y | Y |
| Review | Provides review information on all articles in the system, incl. reviewer names, reviews, and recommendation. | Content | N | Y | Y |

###  **Timed Views Report**

**Availability: OJS 2 only**

**Format: CSV**

**Description:** This report provides overall usage metrics for articles and galley usage. A date span must be specified. It has a legacy and non-legacy mode available. It is the only report that operates in this way.

**Use for**: downloading legacy or non-legacy timed view data.

**Do Not Use for**: downloading data in OJS 3.0+, as it no longer exists. Instead, use the Custom Report Generator.

**Special Notes:**

* Due to the way OJS processes metrics, the report will almost certainly not include data from today’s date, so attempting to report on today’s date only will probably return an empty report.
* This report can optionally provide legacy data for pre-OJS-2.4.3 installs. If you are looking for timed view data from before an OJS 2.4.3 upgrade, select the “include legacy data” option.

**Example Data \(edited for clarity\):**

In the sample below, which was generated for the date span March 29 2017 - March 30 2017 \(ie. 1 day\), we can see that the article “Amusing Ourselves to Death” was quite highly viewed, with 2 abstract views and 11 total galley views \(3 PDF and and 8 HTML\). The “Comobility” article only had its abstract viewed once.  
****

| **ID** | **Article Title** | **Authors** | **Issue** | **Date Published** | **Abstract** | **Total Galley** | **PDF** | **HTML** |
| --- | --- | --- |
| **2**508 | "Amusing Ourselves to Death?" Social Media, Political Satire, and the 2011 Election | Ian Reilly | Vol 36, No 3 \(2011\): Canadian Fascinations | 2011-09-13 22:11 | 2 | 11 | 3 | 8 |
| 2512 | Comobility: How Proximity and Distance Travel Together in Locative Media | Jen Southern | Vol 37, No 1 \(2012\): Media Arts Revisited \(MARs\) | 2012-04-13 9:38 | 1 |  **** |  **** |  **** |





