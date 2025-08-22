---
title: Can QA tests be run against an incomplete system?
---

In addition to why run the tests earlier, the question was how could you even? 
My QA team would ask how can you run tests against an incomplete system, obviously it's incomplete and will fail. 
I think the challenge with understanding the practice of a test being run earlier has to do with the word "test" itself which creates a mental model that doesn't make sense. 
There's a good discussion about the words we use and the mental models they create in [I think this episode of Profound][1], I'll re-listen and update it if it's incorrect.
I think the mental model in people's heads was you test something complete, if it's incomplete, you can't test it.

In manufacturing, there are jigs. 
Jigs are not the tools or the materials, they support the use of tool with the material. 
Testing is inspection. If I were to tell someone to test something before it's finished, obviously it can't be done. 
However the same data (how far a hole should be drilled or at what angle the screw goes into the wood) can be used to make a jig or to do the inspection.
So I explain TDD as JDD or jig driven development. You're basically using the same data to create little jigs (business unit tests). 
I say business unit tests because that's what I think of when I say unit test, not a compilation unit like a class.
There's a good presentation by Ian Cooper [testing the behaviour and not the implementation][2]
I was also using [this set of slides][3] by Thoughtworks as a guide.

The jigs can be mocks that fake parts of the system that aren't ready yet, parts whose absense makes the system incomplete in the local developers environment.
If a mock doesn't apply, you inject the data into a layer like I did with the COBOL database. 
The goal of running the test data through the code is not to check if the code is doing what we want, but to guide the developer so that the code will do what we want. 
This is the same as a jig not being used to check if the hole is drilled in the correct location or angle but to guide the individual in doing so.
I elaborated more about the jig analogy in [Does it matter if the tests actually drive the development?][4]

Assuming your jig (mock or injected data) is correct you should have no defects and this means there's no need to have inspection later on.
You instead inspect the process; that is, you need to test your assumptions about your mocks and there are strategies for that. 
You can inspect the process by running tests or also by managing how you do mocks. 
For example every team should publish a mock for others to use so that downstream teams don't make assumptions about how a dependency works.
I think Bryan Finster describes this in [this episode of Small Batches][5]

QA teams can't know all the layers and the best place to inject the data, only the developers can.
This is why I separated the product (data) from the service (test automation). 
Even at Toyota, they still do inspection at the end as described in [this episode of Lean Made Simple][6].
Some tests still need to be run to inspect the process by inspecting the product and so we still had to make it easier for developers to run those tests in QA.

[1]: https://www.profound-deming.com/profound-podcast/s4-e16-angela-montgomery-integrating-deming-and-goldratt-for-organizational-transformation
[2]: https://www.youtube.com/watch?v=EZ05e7EMOLM
[3]: https://martinfowler.com/articles/microservice-testing/
[4]: 3
[5]: https://smallbatches.fm/38/transcript
[6]: https://www.leanmadesimple.com/podcast/toyota-uk-tour-review
