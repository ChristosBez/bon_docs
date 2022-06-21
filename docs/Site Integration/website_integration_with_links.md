---
sidebar_position: 2
slug : /site_integration/website_integration_with_links
title: Hotel Website Integration with Links
---
# Hotel Website Integration with Links
---

1.	Direct Link 
The easiest way to launch the booking engine is a simple link:
```
https://hotelname.book-onlinenow.net
```
The link is redirected to the 1st step of the booking engine

2.	2nd Step Redirection
To launch the booking engine in the 2nd step directly, the link should follow the format:
```
https://hotelname.book-onlinenow.net/index.aspx?Page=19 
```
The link is redirected to the 2nd step of the booking engine, showing the results of room types and rate plans according to the Default Search Criteria:
```
Arrival date is the current date
Overnights = 1
Adults = 2 (default number of adults configured in back-end)  
```
For example:
```
https://demov3.book-onlinenow.net/index.aspx?Page=19 
```
