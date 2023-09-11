---
title: Rewrite rules are ignored in Safe Haskell
summary: Rewrite rules are not allowed in Safe Haskell and are therefore ignored
severity: warning
introduced: 9.6.1
---

GHC implements the `SafeHaskell` extension which allows programmers to restrict modules to a specific subset which is considered safe and does not contain loopholes such as `unsafePerformIO`.
More details are available in [the GHC User's Guide](https://downloads.haskell.org/ghc/latest/docs/users_guide/exts/safe_haskell.html).
One of the features which isn't considered safe are user-specified rewrite rules. GHC therefore warns that all rewrite rules in a module which is declared safe will be ignored.
