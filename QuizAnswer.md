# Answer for Splunk Quiz - Splunk 7.x Fundamentals Part 1

## Chapter 1 - What is Machine Data
* Machine data is only generated by web servers : **False**
* Machine data makes up for more than **90%** of the data accumulated by organizations.
* Machine data is always structured : **False**

## Chapter 2 - What is Splunk
* What are the three main processing components of Splunk? **Search Heads, Indexers, Forwarders**
* A single-instance deployment of SPlunk Enterprise handles : **Indexing, Parsing, Input, Searching**
> In single-instance deployments, one instance of Splunk Enterprise handles all aspects of processing data, from input through indexing to search
* Search strings are sent from the **Search Head**
* Which function is not a part of a single instance deployment ? **Clustering**
* Search requests are processed by the **Indexers**
* Which of these is not a main component of Splunk ? **Compress and archive**
* In most Splunk deployments, **Forwarders** serve as the primary way data is supplied for indexing.

## Chapter 3 - Installing Splunk
* You can launch and manage apps from the home app. **True**
* The password for a newly installed Splunk instance is **created when you install Splunk Enterprise**
* **Roles** define what users can do in Splunk
* Which apps ship with Splunk Enterprise ? **Search & Reporting / Home App**
* What are the three main default roles in Splunk Enterprise? **Admin / Power / User**

## Chapter 4 - Getting Data In
* In most production environments, **forwarders** will be used as the source of data input.
* Files indexed using the upload input option get indexed **once**.
* The monitor input option will allow you to continuously monitor files. **True**
* Splunk knows where to break the event, where the time stamp is located and how to automatically create field value pairs using these. **Source types**
* Splunk uses **source types** to categorize the type of data being indexed.

## Chapter 5 - Basic Searching
* Events are always returned in chronological order. **False**
* **OR, NOT, AND** are booleans in the Splunk Search Language.
* What is the order of evaluation for Boolean operations in Splunk ? **NOT > OR > AND**
* failed password == failed AND password ? **True**
* How is the asterisk used in Splunk search ? **As a wildcard**
* Shared search jobs remain active for **7days** by default.
* A search job will remain active for **10** minutes after it is run.
* When a search is sent to Splunk, it becomes a **Search job**

## Chapter 6 - Using Fields
* Which is not a comparison operator in Splunk ? **?=**
* Wildcard cannot be used with field searches. **False**
* Field values are case sensitive. **False**
* Field names are **case sensitive**.
* What attributes describe this field : *a* dest **4** ? **It contains 4 string values**

## Chapter 7 - Best Practices
* **@** is the symbol used in the "Advanced" section of the time range picker to round down to nearest unit of specified time.
* Having separate indexed allows : **Faster Searches, Multiple retention policies, Ability to limit access**
* Time to search can only be set by the time range picker. **False**
* What is the most efficient way to filter events in Splunk? **By time**
* As a general practice, exclusion is better than inclusion in a Splunk search. **False**

## Chapter 8 - SPL Fundamentals
* Would the ip column be removed in the results of this search ? Why or why not ? **No, because the name was changed**
> searchtype=a* | rename ip as "User" | fields - ip
* What command would you use to remove the status field from the returned events ? **fields -**
> sourcetype=a* status=404 | fields - status
* Which command removes results with duplicate field values ? **Dedup**
* What is missing from this search ? **Quotation marks around User Ip**
> sourcetype=a* | rename ip as "User Ip" | table User Ip
* Finish the rename command to change the name of the status field to HTTP Status. **status as "HTTP Status"**
> sourcetype=a* status=404 | rename 

## Chapter 9 - Transforming Commands
* To display the most common values in a specific field, what command would you use ? **top**
* How many results are shown by default when using a Top or Rare Command ? **10**
* Which stats function would you use to find the average value of a field ? **avg**
* **List, avg, count, sum** are stats function.
* Which clause would you use to rename the count field ? **as**
> sourcetype=vendor* | stats count ____ "Units Sold"
* **Addtotals** is not a stats function.

## Chapter 10 - Reports and Dashboards
* Charts can be based on numbers, time, or location. **True**
* A time range picker can be included in a report. **True**
* **Admin, Power, User** can create reports.
* **Dashboards** are reports gathered together into a single pane of glass.
* The User role can not create reports. **False**
* If a search return this, you can view the results as a chart. **Statistical values**

## Chapter 11 - Pivot and Datasets
* The instant pivot button is diplayed in the statistics and visualization tabs when a **non-transforming** search is run.
* Which role(s) can create data models ? **Admin, Power**
* Pivots can be saved as dashboard panels. **True**
* These are knowledge objects that provide the data structure for pivot. **Data models**
* Adding child data model objects is like the **AND** Boolean in the Splunk search language.
* Data models are made up of **Datasets**.
* Pivots cannot be saved as reports panels. **False**

## Chapter 12 - Lookups
* External data used by a lookup : Geospatial data, CSV File, Script
* To display data from the http_status.csv : **inputlookup**
* A lookup is categorized as a dataset : **True**
* To keep from overwriting existing fields with your lookup : **OUTPUTNEW**
* The first row in a CSV file for Lookups is the **field name**

## Chapter 13 - Scheduled Reports and Alerts
* Real-time alers will run the search continuously in the background. **True**
* Alerts can be shared to all apps. **True**
* Alerts can send an email. **True**
* Alerts can run uploaded scripts. **True**
* An alert is an action triggered by a **Saved search**.
* Once an alert is created, you can no longer edit its defining search. **False**

## Bonus
* The time stamp you see in the events is based on the time zone in your user account. **True**
* Commands that create statistics and visualizations are called **transforming** commands.
* In a dashboard, a time range picker will only work on panels that include a(n) **inline** search.
