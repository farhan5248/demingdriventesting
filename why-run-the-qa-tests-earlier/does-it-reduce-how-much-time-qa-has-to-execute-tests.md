---
title: Does it reduce how much time QA has to execute tests?
---

In one release, the monolithic build had to go into QA on a fixed date. 
A developer was working with one of my testers in her dev environment but they weren't ready to push the code to QA.
Here were her traditional options:
1. If everyone waited for her, all the other features wouldn't be tested in time
2. If she put whatever code she had, it would create bugs within the system.

Instead I told her to just deploy her DDL changes, that is none of the logic, just changes to file layouts, database tables etc and make sure that it wouldn't break anything. 
I told her that once she was done in that environment, and after merging her code with the rest of the code base and with help from the tester, they could run any related test suites for any features in that release before deploying to QA. 
The result was that they only put the code in once they had virtually defect-free code.
They didn't put the code in QA to test if they had defects. 
The only testing left was integration tests with Oracle DB and Java code etc.
So even though there was a shorter test execution phase, there was significantly less to test.

I say virtually defect-free because we were converting E2E tests to component tests (it helps if you visualise the testing pyramid).
There were two risks with doing this:
1. There weren't many integration tests with the other development teams. 
2. Because of the way the COBOL code itself was integrated before going into QA, not much testing was done after the integration.

My team was not that comfortable with not running the tests in QA since we still had to sign-off. 
As a result we wound up implementing the [Test Hourglass anti-pattern][1].
In the end, hundreds of test cases per feature could run in minutes so there was no downside to just re-running the same tests. Not ideal but it worked.

At this point the COBOL testers realised that they could basically work side by side with developers in the lower environments until they were satisfied. 
Then one by one, they'd integrate and test and deploy code to QA only as the tester was ready to do any integration tests. 
They'd also schedule it such that it would be done just before the deploy to the customer facing environments. 
One tester estimated they'd only be in QA for 2 days (automated regression cycle) per feature instead of the 3 months.
They were slowly getting how Continuous delivery would work.

[1]: https://testing.googleblog.com/2020/11/fixing-test-hourglass.html
