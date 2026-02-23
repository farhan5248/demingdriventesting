---
title: Can all the end-to-end tests be run earlier?
---

The short answer is yes but you'd have to validate assumptions at some point.

When I was in my dev team, we used to run our own end-to-end tests in QA after each deploy to the environment.
If I was deploying code for a specific component, I'd route all traffic to and from it through Hoverfly to capture the requests and responses.
Then we're run the end-to-end test suite. Now that we had all inputs and outputs, we could simulate any dependencies in a lower environment, like a developer's laptop. What we also had to do concurrently is make sure that those dependencies, typically hosted by external organisations, were returning the response we had captured. So we'd test those endpoints directly against the previously captured response. 

If the dependency was developed locally, then we'd make our own mocks and test a service against it's own mock. 
If the implementation changed, the mock service was updated which would trigger tests to run on downstream projects.

And if you're not working with services but databases instead? 
When I was on the QA team, there was this project with a 7 character field. If I remember correctly it could be one of 3 things, a drug number, a group number with a prefix or a 6 digit date of birth with a prefix. 
When the testers and developers tested their code, they made assumptions about where the prefix would be and tested all the logic that depended on it.
When the code was deployed to QA, they had the first opportunity to test that field with the upstream components that provide its data. 
They didn't need to re-test everything, they just tested the mapping of drugs, groups and DOB to that field.
They found a defect, regenerated the test automation and fixed the code in the lower environment.