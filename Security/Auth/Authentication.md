Differently from [[Authorization]], authentication is about identity verification, which means it will try to answer "Who am I?".

Authentication validates credentials (such as passwords, keys, or tokens) and establishes trust in an identity.

A useful mental model is to treat authentication as an **event**, not an application state. Once credentials are verified, authentication is complete and may produce artifacts (sessions, tokens, claims) that can be used later.

This conceptual abstraction is important in modern auth systems, especially in stateless and distributed architectures.

> Authentication happens.

