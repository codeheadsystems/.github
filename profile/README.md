
# Codehead Systems

A collection of software built by programmer Ned Wolpert

## How to Contact Ned
- <a rel="me" href="https://hachyderm.io/@CodeHead">Mastodon</a>
- <a href="https://github.com/wolpert">github</a>
- <a href="https://www.linkedin.com/in/wolpert">Linkedin</a>
- email: ned dot wolpert at gmail dot com


## The Codehead Projects

All projects listed here are Apache 2 licensed open-source.


* [the Hofmann Elimination](https://github.com/codeheadsystems/hofmann-elimination)

In an effort to reduce the attack surface for websites with login credentials,
I implemented OPAQUE/OPRF from RFC specs. OPAQUE removes the need to send the
private key material (passwords, etc) to the website and yet still provide
strong authentication for login. It does this by using the OPRF protocol and
elliptic curves for hashing. All 3 RFCs that are involved with this protocol
have been implemented in Java using Bouncy Castle as the core. Updates will
include having JavaScript clients and, in the future, implementations in 
other languages like Rust, Go and C# with full testing libraries. 


* [The Libraries](https://github.com/codeheadsystems/libraries/)
Various open-source Java libraries, including:

	* [Feature-Flag](https://github.com/codeheadsystems/libraries/tree/main/feature-flag)

	A utility I built for svarm, but put into it's own project to share
	it.  It's an implementation of A/B testing using the simplistic
	'Feature Toggle' idea Martin Fowler wrote about years ago. I used
	something similar back in Amazon when I was on the Alexa
	project. Amazon had a full-feature A/B library, but it was
	over-bearing so Alexa devs made a simpler one. This is based on that
	one.

    * [CodeHead Test](https://github.com/codeheadsystems/libraries/tree/main/codehead-test)

	Provides test utilities I use. Generally around Jupiter, immutables and
	jackson. Small, easy to consume.


	* [Database Test](https://github.com/codeheadsystems/libraries/tree/main/database-test)

	Test utilities I have around databases. Mostly around cassandra and unique
	strings. Moved out of codehead-test because they are really specialized.

	* [Metrics](https://github.com/codeheadsystems/libraries/tree/main/metrics)

	Dropwizard/Micrometer integration with dagger support. Helper utilities
	including help for unit tests with code that use metrics.

	* [OOP Mock](https://github.com/codeheadsystems/libraries/tree/main/oop-mock)

	Out of process mock facilities. Gives you the ability to mock downstream dependencies
	in your functional tests. Useful if you want to separate out service level
	tests from external integration frameworks. Ideal for those who have separate
	tests for functional and integration. I built this because I as an ex-amazon
	developer, I missed the internal project called Chameleon.

	* [State Machine Redux](https://github.com/codeheadsystems/libraries/tree/main/smr)

	A simpler state machine project. I realized the previous one got a bit out
	of hand. This one is easy to use, allows for the import/export of state
	machines, but more viable for games as well as larger projects. The KISS
	version.

	* [Local Queue](https://github.com/codeheadsystems/libraries/tree/main/local-queue)
