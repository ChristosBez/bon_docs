---
sidebar_position: 2
slug : /site_integration/website_integration_with_booking_form
title: Hotel Website Integration with Booking Form (mask)
---
# Hotel Website Integration with Booking Form
---

### 1.1 Booking Mask with one kid category (mostly used)

There is a set of parameters needed to link a website through a booking form to the
2nd step of the booking engine. These parameters are explained below in detail.

| **Name**         | **Type** | **Values** | **Required** | **Example**          | **Notes**                                  |
| ---------------- | -------- | ---------- | ------------ | -------------------- | ------------------------------------------ |
| **Page**         | Int      | 19         | Yes          | Page=19              | Fixed value = 19                           |
| **lan_id**       | String   |            | Yes          | lan_id = en-US       | Selected Language <br/><br/>see Appendix I |
| **src**          | Int      |            | No           |                      | Booking Source <br/><br/>see Appendix II   |
| **promo**        | String   |            | No           |                      | Promo Code or Agent Code                   |
| **arrival**      | Date     |            | Yes          | arrival = 29/05/2013 | Format <br/><br/>dd/MM/yyyy                |
| **departure**    | Date     |            | Yes          |                      | Format <br/><br/>dd/MM/yyyy                |
| **rooms**        | Int      |            | Yes          | rooms = 1            | Number of Rooms                            |
| **adults**       | Int      |            | Yes          | adults = 3           | Number of Adults                           |
| **kids**         | Int      |            | Yes          | kids = 1             | Number of Children                         |
| **kid1**         | Int      |            | Yes          | kid1 = 1             | Active kid category                        |
| **kid2**         | Int      |            | Yes          | kid1 = -1            | Active kid category                        |
| **kid3**         | Int      |            | Yes          | kid1 = -1            | Always -1 – NOT USED                       |
| **selectedroom** | String   |            | No           |                      | Room Type Abbreviation                     |

The booking form is linked with the booking engine only with one kid category.
For example, if the kid1 category (i.e. 0-6) is free of charge and you want to link only
the second kid category (i.e. 7-12), then the parameters kid1, kid2, kid3 should be
set as follows:

kid1=-1, kid2=1, kid3=-1

Below is an example of the booking engine URL with all needed parameters:
```
https://demov3.book-onlinenow.net/index.aspx?Page=19&lan_id=&arrival=26/05/20 20 &departure=28//20 20 &rooms=1&adults=3&kids=1&kid1=-1&kid2=1&kid3=-1&extra=0&cot=
```

### 1. 2 Booking Mask with two kids categories

There is a set of parameters needed to link a website through a booking form to the
2 nd step of the booking engine. These parameters are explained below in detail.

| **Name**         | **Type** | **Values** | **Required** | **Example**          | **Notes**                                                       |
| ---------------- | -------- | ---------- | ------------ | -------------------- | --------------------------------------------------------------- |
| **Page**         | Int      | 19         | Yes          | Page = 19            | Fixed value = 19                                                |
| **lan_id**       | String   |            | Yes          | lan_id = en-US       | Selected Language <br/><br/>see Appendix 1                      |
| **src**          | Int      |            | No           |                      | Booking Source                                                  |
| **promo**        | String   |            | No           |                      | Promo Code or Agent Code                                        |
| **arrival**      | Date     |            | Yes          | arrival = 29/05/2013 | Format <br/><br/>dd/MM/yyyy                                     |
| **departure**    | Date     |            | Yes          |                      | Format <br/><br/>dd/MM/yyyy                                     |
| **rooms**        | Int      |            | Yes          | rooms = 1            | Number of Rooms                                                 |
| **adults**       | Int      |            | Yes          | adults = 3           | Number of Adults                                                |
| **kid1**         | Int      |            | Yes          | kid1 = 1             | Number of kids of the 1st kid category                          |
| **kid2**         | Int      |            | Yes          | kid1 = -1            | Number of kids of the 2nd kid category <br/><br/>see Appendix 3 |
| **kid3**         | Int      |            | Yes          | kid1 = -1            | Always -1                                                       |
| **selectedroom** | String   |            | No           |                      | Room Type Abbreviation                                          |
| **Extra**        | Int      | 0          | Yes          |                      | Fixed value = 0                                                 |
| **cot**          | Int      | 0          | Yes          |                      | Fixed value = 0                                                 |


### 1.3 Wordpress sites - Installation Instructions (suggested)

For installation of the mask (horizontal or vertical) in a Wordpress website the following steps should be followed:

1. Copy the _/css_ in your main directory of your website

2. In Wordpress Admin, go to _Plugins_ and install the plugin RAW-HTML
(https://wordpress.org/plugins/raw-html/ ) or any similar plugin

3. In Wordpress Admin, go to _Appearance-> Widgets_ and add a text widget to your Page Widget Area.

a. Inside the _text widget_ , do copy paste the code from the file " _Booking.html_ ".
b. Add in the first line the following command:
```<!--raw-->```
And after the last line add the following command:
```<!--/raw-->```
So the text area should start with **```<!--raw-->```** and end with **```<!--/raw-->```**.