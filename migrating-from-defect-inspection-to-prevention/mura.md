---
title:  Mura - Unevenness
---

Though I had come across the term [SPC][1] I didn't know anyone who knew anything about them.
As a result, I basically had this one type of chart that I used the entire 4.5 years I was on the QA team.
I looked at this myself and sometimes drew it out for people but rarely referred to it in any meeting with anyone.
Looking back I can describe the transformation journey of the COBOL testers using these charts.

Imagine each one is for a feature that lasts 3 months; everyone on the team had at least one of these at any point of time.
The x axis is time from the moment the tester started writing test cases.
The y axis is time it takes to correct a failure. 
Some failures were due to code bugs but others were test planning failures.
Examples of test planning failures are incorrect test case expectations or typos in the test case which create errors in the test automation generation.

I'll draw nice pictures later but put Ascii art for now :P
```
Legend:
- : Day without failures
^ : Test planning failure which needs less than a day to fix
/\ : Code bug which needs more than a day to fix
//\\ : regression defect (takes several days to fix due to context switching or troubleshooting)
```

In the beginning all the tests were written, then executed manually when the code was deployed and then automation created for the regression and run right at the end.
What you'd see is long delays between code bugs caused by manual time consuming inspection with tests passing.
Manually executing the tests wasn't the only reason for the delays between finding bugs, it was having to re-work the test cases that had incorrect expectations.
At the end you'd have regression suite failures that take even longer to fix because by then the developers have moved onto next project.
When I think about this type of re-working of the tests, I think of the story about the [Toyoda looms][2]
```
|  dev       || qa                       || reg  | 
--------------/\-^-^/\-^-^/\-^-^/\-^-^/\/\//\\//\\
```

One of the first things we did was create the automation after all the tests were written instead of at the end.
This was when I introduced the term [Jidoka](jidoka) and automated the creation of test automation.
This made the delays due to manual execution basically disappear and now the tester was either logging defects or fixing test cases.

```
|  dev       || qa               || reg  | 
--------------/\^^/\^^/\^^/\^^/\/\//\\//\\
```

Next we tried to mistake proof writing test cases to eliminate automation generation errors.
That's when I introduced [Poka Yoke](poka-yoke). 
If the code was delivered to QA before we finished writing all the tests, then we ran what we had.
This was done to prevent re-work in the test case expectations.
There were still some tests that had to be re-worked but not as many.
```
|  dev       || qa           || reg  | 
--------------/\^/\^/\^/\/\/\//\\//\\
```

Finally the testers and developers were writing their tests and running them in small batches daily and sometimes hourly in the lowest dev environment.
There was re-work but none that I could detect because almost all issues were fixed within the day.
By this point I had explained [Just In Time](just-in-time) to the team.
Most regressions were run in the dev environment but some data was only available in QA. 
There were still regression defects or integration defects with the non COBOL system. 
The former were quickly fixed and the latter I treated as special cause variation. 
The code was delivered to QA later at this point, but the whole process was smoother and we were still done ahead of schedule.
```
|  dev              || qa + reg  | 
---------------------/\---------/\
```

[1]: https://deming.org/the-first-control-chart/
[2]: https://www.toyota-global.com/company/history_of_toyota/75years/text/taking_on_the_automotive_business/chapter1/section1/item4.html
