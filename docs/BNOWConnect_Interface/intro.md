---
sidebar_position: 3
slug : /bnowconnect_interface
title: BNΟWConnect Interface Specification
---

# Introduction

This document provides information on integrating *Central* *Reservation
System* (CRS) or a *Property Management System* (PMS) with
BookOnlineNow. BookOnlineNow is the leading Booking Engine solution.

*BNOWConnect* is a set of services for *Property Management System*
(PMS) systems to connect with BookOnlineNow. As availability and rates
change, the PMS would send updates using *BNOWConnect* to the booking
engine. As bookings/reservations are made by consumers, *BNOWConnect*
would make available the reservations to the PMS using a reservation
pull mechanism.

Section 2 of this document specifies the interface that PMS needs
implement to push update messages to the booking engine.

Section 3 of this document specifies the interface that *BnοwConnect*
makes available to PMS to pull reservations.