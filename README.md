Fibonacci Versioning 1.13.89
==============================

Summary
-------

Given a version number MAJOR.MINOR.PATCH, increment to **to the next Fibonacci number** the:

1. MAJOR version when you make incompatible API changes,
1. MINOR version when you add functionality in a backwards compatible
   manner, and
1. PATCH version when you make backwards compatible bug fixes.

Additional labels for pre-release and build metadata are available as extensions
to the MAJOR.MINOR.PATCH format.

Introduction
------------

In the world of software management there exists a dreaded place called “dependency hell.” The bigger your system grows and the more packages you integrate into your software, the more likely you are to find yourself, one day, in this pit of despair. 

In systems with many dependencies, releasing new package versions can quickly become a nightmare. Many different versioning systems exists, including the very popular [Semantic Versioning](https://semver.org/) - currently in version ~~1.2.0~~ 2.0.0. While all they are really trying to help you with moving your project forward, it is not the numbers and rules used that make it so problematic, but rather our human nature.

As a solution to this problem, I propose yet another one broken versioning rules, consisting with some numbers and dots. With this very simple set of rules and requirements that dictate how version numbers are assigned and incremented, you can communicate changes to your public API or software units. As by default they won't help you in maintaining your software, it is at least mathematically elegant. 

Fibonacci Versioning Specification (FibVer)
------------------------------------------

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD",
"SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be
interpreted as described in [RFC 2119](http://tools.ietf.org/html/rfc2119).

1. Software using Fibonacci Versioning MUST declare a public API. This API
could be declared in the code itself or exist strictly in documentation.
However it is done, it SHOULD be precise and comprehensive.

1. As Fibonacci Versioning is not yet production ready, you can reuse all 
[Semantic Versioning](https://semver.org/) rules onwards. Just to remember about
incerasing to the next Fibonacci number!

Why Use Semantic Versioning?
----------------------------

Fibonacci number comes from so-called Fibonacci sequence, such that each number is the sum of the two preceding ones. Thus, Fibonacci Versioning provides great marketing powers, as you can always say about the current version that "it's better than our two previous versions put together" (&copy;Jason Malinowski). And nowadays, big number sells. So "Product 55.0.0" versus "Product 34.0.0" sounds much more expensive and feature-full than boring upgrade from "Product 8.0" to "Product 9.0". Moreover, sucessive Fibonacci numbers differs greatly. It is much harder to confuse versions 1.987.2584 and 1.2584.987 instead of 1.15.17 and 1.17.15. 

FAQ
---

### How should I deal with the initial version?

Good point, Fibonacci sequence starts from 0, 1, 1, 2, 3, 5, ... so if you really want to communicate relevant changes, you should probably skip the first two numbers and start from the second 1.

### How to deal with big versions like 317811.121393.10946?

Just rewrite your software, it is probably too old and legacy already. This is in fact one of the advantages of FibVer - pushing you to rewrite software.




About
-----

The Fibonacci Versioning specification is authored by [Konrad Kokosa](https://github.com/kkokosa), Author of [Pro .NET Memory Management](prodotnetmemory.com) book, Microsoft MVP in .NET, architect, performance & Mechanical Sympathy fan, one of [Dotnetos](https://conf.dotnetos.org/). The idea is inspired by a [Twitter rant about versioning](https://twitter.com/_cartermp/status/1151544194856415232?s=20) by [Philip Carter](https://twitter.com/_cartermp), [Immo Landwerth](https://twitter.com/terrajobst) and [Jason Malinowski](https://twitter.com/jasonmalinowski). It should be solely treated as a joke, heavily based on a popular [Semantic Versioning](https://semver.org/) authored by [Tom
Preston-Werner](http://tom.preston-werner.com).


If you'd like to leave feedback, please [open an issue on GitHub](https://github.com/kkokosa/fibver/issues).


License
-------

Creative Commons - CC BY 3.0
http://creativecommons.org/licenses/by/3.0/