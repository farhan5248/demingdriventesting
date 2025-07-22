---
layout: page
title:  Dr Deming
permalink: /deming/
---

I figured I'd make this summary for anyone unfamiliar with Dr Deming.
You can Google him and visit the [Deming Institute site](https://deming.org/) but I wanted to cover his relevance to software development and QA especially.

How did I come across him? As I mentioned in the [About](/about) section his name kept coming up when I started my research around 2018.
It was mainly in books but the last source was the site which explained the term shift left using the burnt toast analogy.

On his Profound Podcast, John Willis often says it all goes back to Deming. 
If you listen to Dr Steven Spear, Gene Kim, Jez Humble, Dave Farley, the Poppendiecks, they'll talk about Lean, Toyota or [NUMMI](https://www.thisamericanlife.org/561/nummi-2015). Andrew Clay Shafer is one of the people who coined the phrase DevOps. 
He's directly referenced Dr Deming in [this presentation](https://www.youtube.com/watch?v=C8hma_YSBX0&t=3s)

You can read about the relationship between Dr Deming and Toyota [here](https://deming.org/toyotas-management-history/).
The [Sys-Tao site has some good links](https://sys-tao.org/links/), these are about Dr Deming.
1. [If Japan Can, Why Can't We?](https://www.youtube.com/watch?v=vcG_Pmt_Ny4)
2. [W. Edwards Deming - Part 1](https://www.youtube.com/watch?v=GHvnIm9UEoQ)

You can find the list of 14 points [here](https://deming.org/explore/fourteen-points/). 
I've put some comments on the ones that applied to my QA team.
11 and 12 have two parts, I only put the part that I could apply.
The same goes for point 4, I didn't attempt to apply that.

1. **Create constancy of purpose toward improvement of product and service, with the aim to become competitive and to stay in business, and to provide jobs.** The product my team was trying to improve was data they create for consumption by developers via the API and the service was feedback through automated tests that the developers could also run. Their goal was to keep their jobs in Canada by showing they could be more productive. My team sized reduced from under 60 to under 30 in that time.

2. **Adopt the new philosophy. We are in a new economic age. Western management must awaken to the challenge, must learn their responsibilities, and take on leadership for change.** My job from the moment I joined the team was to change the way they worked. Inspection on the scale they were used to had to stop. The minute I finished changing my team, I handed the reigns to one my team-leads and quit my job.

3. **Cease dependence on inspection to achieve quality. Eliminate the need for inspection on a mass basis by building quality into the product in the first place.** This was interpreted as implementing shift-left. It was simply the cool buzzword at the time so I used it. Most of the work done by the COBOL code QA team was around this, they got to the point of not needing inspection in QA because they worked with the developers to run the tests every daily and even hourly during the coding phase. Though only the COBOL developers ran the tests, every QA tester on my team had developed the same skills working towards the goal of ceasing dependency on mass inspection.

5. **Improve constantly and forever the system of production and service, to improve quality and productivity, and thus constantly decrease costs.** I interpreted this as how you achieve point 1. When I started in 2018, I made 1 or maybe 2 improvements and twiddled my thumbs most of the time waiting for suggestions. By the time I left, there was a backlog of improvements that me and 3 of my developers just didn't have the time for. We were pushing out changes to the Maven or Xtext plug-ins everyday.

6. **Institute training on the job.** I met every single person on my team for 1:1 every week. That's right, that's like dozens of meetings weekly :) Initially it was for 30 minutes per person, then it was only for full-time employees after most contractors left, then it was pairs of folks because my throat needed a break from talking every 30 minutes. The 1:1 was simple, it was for me to ask what [Paul Akers I believe asked folks, what about your job is bugging you](https://paulakers.net/2011/general/fix-what-bugs-you). I personally trained everyone on my team until I needed to pass on the responsibility to others as I planned on leaving.

7. **Institute leadership. The aim of supervision should be to help people and machines and gadgets to do a better job. Supervision of management is in need of overhaul, as well as supervision of production workers.** I didn't do the job of managing my QA team like its previous managers. I instead coached my team-leads on how to make decisions without me by providing data and clear guidelines. I instead managed the system of work. I wanted my 3 team-leads at the time to be completely autonomous and reach out to each other when they needed help.

8. **Drive out fear, so that everyone may work effectively for the company.** Just as you have upper case Agile which is not the one you want. This place was upper case Pathological, which isn't the pathological you want :) . To me this was about creating pyschological safety. That said, in the beginning I had to use the fear of them losing their jobs to motivate them to learn new skills. What I had told them is that whether they disagree or agree with me, either was fine, as long as they went through an informal PDCA cycle. Having everyone agree with me isn't necessarily a good thing if it's out of fear. I wanted them to see that I value them following the scientific method when it came to doing their work more than I valued them agreeing with me; I'm not right all the time afterall.

9. **Break down barriers between departments. People in research, design, sales, and production must work as a team, to foresee problems of production and in use that may be encountered with the product or service.** Within my QA team, there were barrier and I broke those down. The 3 team-leads could self organise to help each other solve problems. Before this, there would be duplicated testing effort between my teams as each tried to maximise the time they got for their project.

10. **Eliminate slogans, exhortations, and targets for the work force asking for zero defects and new levels of productivity. Such exhortations only create adversarial relationships, as the bulk of the causes of low quality and low productivity belong to the system and thus lie beyond the power of the work force.** Inspection doesn't ensure quality so setting targets to find defects seemed pointless to me. Rewarding folks for finding defects is basically the red bead game so I stopped that. I got the impression that the culture in QA teams is that the person who find the most defects is the hero and this is seen as desirable. This was the opposite of defect prevention which was asking my testers to work in a way that they find no defects. This doesn't mean I set a target of 0 defects, just that we were going to work towards a goal in the opposite direction of what they were used to.

11. **Eliminate work standards (quotas) on the factory floor. Substitute leadership.** This was another weird thing, at least for me, a developer in the QA world, somehow given a feature, there was an expectation of x number of tests should be written at least. It was like if you had a developer work for 10 days, then you have a quote of 10 test cases and there was actually a number in some estimation formulas of the number of test cases they should write a day. That's like have a number for the amount of lines of code a developer should write per day. I get that it was an estimation formula but I eliminated expectations like these where I could. Instead I wanted a just-in-time approach of a tester making only as many test cases as a developer would need for red-green-refactor and BDD.

12. **Remove barriers that rob the hourly worker of his right to pride of workmanship. The responsibility of supervisors must be changed from sheer numbers to quality.**
This was simple, instead of lots of test cases written for the impossible goal of inspecting quality in, I wanted the testers to take the time to come up with better quality test cases even if that meant there were fewer of them. If that was good enough for a developer to build the right thing, then we didn't need these huge inventories of test cases whose creation time was basically a non-value added activity.

13. **Institute a vigorous program of education and self-improvement.** I blocked out 3 hours and then 1 hour on folks calendar so they could read or learn something new each week. That unfortunately didn't take; people just kept working. So later, we developed an environment were you'd learn through experimentation when you were trying your new Kaizen.

14. **Put everybody in the company to work to accomplish the transformation. The transformation is everybody's job.**
I wasn't the CEO, but I certainly made sure everybody on my team was part of the transformation. Nobody was getting carried; supported yes, carried no. This is because they were improving themselves, it's like nobody can go to the gym for you, you have to do the work yourself and yes, it's hard.