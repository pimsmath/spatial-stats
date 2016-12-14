---
date: 2016-12-07T14:36:21-08:00
title: Gantt
weight: 30
---


<p align="right">
    <a href="/logistics/"><i class="fa fa-check-square fa-2x" aria-hidden="true"></i></a>
    <a href="/crowdmark/gantt/"><i class="fa fa-tasks fa-2x" aria-hidden="true"></i></a>
</p>

{{< mermaid >}}
gantt 
    dateFormat YYYY-MM-DD 
    title 2017 Spatial Stats Course Action Plan 

    section Milestones 
    Dec. 1 :crit, admin6, 2017-12-01, 1d 
    Nov. 1 :crit, admin 5, 2017-11-01, 1d 
    Oct. 1 :crit, admin4, 2017-10-01, 1d 
    Sep. 1 :crit, admin3, 2017-09-01, 1d 
    Aug. 1 :crit, admin2, 2017-08-01, 1d 
    Jul. 1 :crit, admin8, 2017-07-01, 1d 
    Jun. 1 :crit, admin7, 2017-06-01, 1d 
    May. 1 :crit, admin6, 2017-05-01, 1d 
    Apr. 1 :crit, admin 5, 2017-04-01, 1d 
    Mar. 1 :crit, admin4, 2017-03-01, 1d 
    Feb. 1 :crit, admin3, 2017-02-01, 1d 
    Jan. 1 :crit, admin2, 2017-01-01, 1d 
    

    section Admin 
    Video Testing   :crit, admin10, 2017-08-01, 2017-08-15
    Announcement     :active, admin9, 2017-01-08, 1d
    Western Dean's   :active, admin14, 2017-01-01, 2017-01-12
    Message         :active, admin11, 2016-12-14, 1d

    section Technology
    video conferencing  :active, tech1, 2017-02-01, 2017-04-01
    GitHub  :active, tech2, 2017-01-015, 2017-03-15
    Jupyter :active, tech3, 2016-12-15, 2017-03-01

    section Data
    unknown :active, data1, 2017-01-15, 2017-02-01

    section Course
    course runs     :active, course1, 2017-09-01, 2017-12-15

{{< /mermaid >}}
