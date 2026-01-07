# Test-Driven Development

TDD is a software development technique that emphasizes better code design using short feedback-loops using automated tests.

Often, TDD is remembered as _the_ test-first technique to go to, but TDD can be resumed to so. As a methodology, TDD is much more about code design than testing; tests are just used as a tool towards better code design. Yes, we often end up with good tests, but that is a side-effect of the process, not the goal. But, is not wrong to use TDD to get tests, but nowadays there are better techniques to get good tests. See [Test-Driven Development](https://martinfowler.com/bliki/TestDrivenDevelopment.html):

> Writing the test first, what XPE2 calls Test-First Programming, provides two main benefits. Most obviously it's a way to get SelfTestingCode, since we can only write some functional code in response to making a test pass. The second benefit is that thinking about the test first forces us to think about the interface to the code first. This focus on interface and how you use a class helps us separate interface from implementation, a key element of good design that many programmers struggle with.

What makes TDD special is the "Red-Green-Refactor" feedback-loop mentioned:

- Write a test for the next bit of functionality you want to add.
- Write the functional code until the test passes.
- Refactor both new and old code to make it well structured.

