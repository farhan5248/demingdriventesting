---
title:  Muri - Overburden
---

Before I started the transformation some testers were always busy; there was almost a hero culture.
What made them busy?
1. Doing the more difficult features/prod bugs. The more complex a feature, the more the mental models and expectations of what the system should do deviated. This mean more discussions and back and forth with the BSA to clarify requirements written months ago.
2. Helping team-mates. The more senior testers gladly helped more junior ones even if they had to work overtime for free.
3. Increasing the scope of testing to find more bugs if they didn't find enough bugs. There was this culture that the good testers find bugs so if someone didn't find any bugs, they felt they need to fill their bugs found quota.  This was easy for me, I just told them I didn't care about finding bugs because quality can't be inspected in.  
4. Retesting buggy code which took multiple attempts to fix. Each time they re-ran a test, it required them to switch context to different functionality and pay attention to it's subtle differences. Just as developers shouldn't be interrupted every hour, I'd say this applies to testers writing tests or investigating failures.
5. Researching current behaviour by examing previous tests. Tests were stored by projects and not product functionality so it would take a while to go through all of those tests to find what was missing.
6. Admin tasks like recording how many tests they ran or wrote each day.
To me, that was like tracking how many lines of code a developer writes or deploys each day; pointless.
After I left, I'm told, they were told to return to this practice and add what percentage they automated.  
I'm told this instruction from the top, like the C-suite but without any explanation why.

By the time I left, an example of overburden was the use of Cucumber. 
When a test fails in Cucumber, the stack trace isn't easy for someone to go through.
I concluded that the team needed to leave Cucumber behind which is why my example project demonstrates how to write the tests in AsciiDoctor.
I wrote more about it on the [blog](/sheepdogblog/engineering-room/2025/08/04/how-we-made-minecraft-using-continuous-delivery)