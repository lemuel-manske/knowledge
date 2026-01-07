# Testing

## 1st: Testing is not the same as [[TestAutomation]].

Dan North has a beautiful article on this topic: [We need to talk about testing](https://dannorth.net/blog/we-need-to-talk-about-testing/).

The industry has been confusing the need to [[TestAutomation]] with the need to [[Testing]] itself for too long. Dan explains the automation necessity and also the human testing necessity as _both_ playing different but important roles in software development.

> [...] Why don’t we automate all the testing? We should write automated tests when they can help surface evidence, especially for something we are likely to do again and again, and we should do this from a testing perspective rather than a programmer guidepost perspective. [...] A human being is doing much more than pressing buttons when they interact with a computer system, and the insights and feedback they can produce make hands-on testing a valuable ongoing activity.

The hierarchy that "agile" has popularized (programmers > automated testers > manual testers) is harmful to software development.

Back in the article, he also puts (as an anti-pattern):

> We only need testers to mop up after us; to do the testing that is too expensive to automate, or which changes too often to be worth it. We will call this manual testing.

The industry lacks some real *good* testers. No talking about the roles, but the mindset and skills to test software effectively (automation is just a tool on a good tester's belt)

> When and where should we be testing? [...] As early as possible and as often as is practical; wherever in the development cycle we can start surfacing evidence to give assurance. Programmers should be thinking like testers at least some of the time, and testers can help them with this.

Nowadays, testing can be used to put the software on the lens of very different perspectives, like security, performance, usability, accessibility, etc.

As developers we try to automate it all (when aligned to Dan's view, this is not a bad thing). But we should not forget that testing is a human activity as well, and that humans can find things that automation cannot (yet) find. Automation works on evidence-based-feedback-loops, but humans can use heuristics, exploratory techniques, and other cognitive skills to find problems that automation cannot find.

# Techniques

_One can devote his entire career on testing._

A very powerfull technique is so called [[PropertyBasedTesting]]: a specialization of [[UnitTesting]] where the tests are generated based on invariants satisfied (expected to) by the SUT on random inputs (properties).
PBT is much about finding the appropriate properties to test, and the right way to generate inputs, or will end up with useless suites. From this very brief description, [[PropertyBasedTesting]] communicates well with [[DesignByContract]] concepts.

