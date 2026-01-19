Authorization is about access control. Here, "Who am I?" (from [[Authentication]]) it's not what matters, but "What am I allowed to do?".

Authorization evaluates permissions, roles, scopes, or policies to decide whether a given action on a resource is allowed.

A common misconception is that authorization always requires authentication first. In reality, **authorization can exist independently of authentication**. Many systems authorize actions without a verified identity (for example, guest users, API keys, or public access with limited permissions).

Authorization is typically evaluated **continuously**, often on every request.

Authorization is standardized by [[OAuth]].

> Authorization continues.

