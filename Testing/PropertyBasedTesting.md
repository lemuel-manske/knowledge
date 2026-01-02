> **Don’t write tests, generate them.**

Property-Based Testing (PBT) is a testing technique where tests are *generated* from **properties** (invariants) that the System Under Test (SUT) must satisfy. Instead of writing individual test cases with fixed inputs and expected outputs, the tester specifies general laws about the system’s behavior, and the framework generates many inputs — often including *sequences of operations* — to try to falsify those laws.

PBT became popular alongside [[FunctionalProgramming]], where immutability, purity, and expressive type systems make properties easier to define and reason about. The Haskell library [QuickCheck](https://hackage.haskell.org/package/QuickCheck), created in 1999 by Koen Claessen and John Hughes, is usually cited as the first widely known PBT framework.

The real power of PBT does not come from random data generation alone, but from **well-chosen properties and a clear model of the system**. Weak or meaningless properties lead to shallow tests. At its strongest, PBT tests *histories of interactions*, not just isolated input/output pairs.

As discussed in [The Sad State of Property-Based Testing](https://stevana.github.io/the_sad_state_of_property-based_testing_libraries.html), many modern PBT frameworks focus mainly on stateless testing and data generation, while offering limited support for **model-based stateful testing** and little to no support for **concurrency testing with formal oracles**.

PBT shines in languages with **expressive type systems**, especially dependently typed languages like Idris and Agda, and in functional languages such as Haskell and Erlang, where types, models, and properties naturally reinforce each other.

