-------------------------
### Run bitwrk-Google-Colab

https://colab.research.google.com/drive/1OShIMVcFZ_khsUIBOIV1lzrqAGo1gfm_?usp=sharing

-------------------------

[![5 Minute introduction to BitWrk](https://img.youtube.com/vi/KmwcxwhIRr0/0.jpg)](https://www.youtube.com/watch?v=KmwcxwhIRr0)

Artists use [Blender](http://blender.org), a powerful yet free 3D software, to create impressive
pictures and movies. This requires a time-consuming, and costly, production step called _rendering_.

BitWrk integrates with Blender and makes rendering much quicker by dispatching it to a swarm of
computers. 

By creating a _marketplace for computing power_, BitWrk introduces a new kind of
_cloud computing_, in which resources are shared in a peer-to-peer fashion. It
works like a stock exchange, using crypto currency [Bitcoin](https://bitcoin.org/)
for payment.

This is interesting for two groups of people:
- The **buyers**: Users who require lots of computing power at their finger tips.
- The **sellers**: Hardware owners who have computing power to spare and would like to
  monetize that resource.

BitWrk provides a service to both groups by connecting them in an easy-to-use way.

### On the web
[bitwrk.net](https://bitwrk.net/) | [Download](https://github.com/indyjo/bitwrk/releases) | [Facebook](https://www.facebook.com/bitwrk) | [Twitter](https://twitter.com/BitWrk)

### Documentation
[News](NEWS.md) | [Quickstart instructions](QUICKSTART.md) | [Concepts](CONCEPTS.md) | [Compiling](COMPILING.md) | [License information](COPYING)

### Stargazers over time

[![Stargazers over time](https://starchart.cc/indyjo/bitwrk.svg)](https://starchart.cc/indyjo/bitwrk)

Status
------

As of version 0.6.5:
- BitWrk concentrates on the use case of providing peer-to-peer rendering for [Blender](http://blender.org),
  the free rendering software, into which it integrates by use of an add-on. Local network and swarm rendering
  can be combined. GPU rendering is supported, too.
- BitWrk is now integrated with a Bitcoin payment processing system, allowing users to pay for
  compute power, in Bitcoin. For this, the user has to request a deposit address, which will
  be provided after a couple of seconds by the payment processor. Bitcoin transactions need at
  least 6 confirmations, i.e. depositing on BitWrk takes one hour on average. Withdrawals aren't
  enabled yet for security reasons. Users are advised to keep the amount of money stored on BitWrk
  as small as possible (deposits can be as small as 0.001 BTC!). Of course, a pay-out can be
  triggered manually by the developer. Ask him!
- There is a central service, written in Go (http://golang.org/) and based on Google AppEngine.
  It exports an API for entering bids and updating transactions. Every transaction's lifecycle can
  be traced, and all communication is secured with Elliptic-Curve cryptographic
  signatures. These are of the same kind than those that can be generated using
  the original Bitcoin client, so it is very easy to test for correctness.
- A client (also called the "daemon"), written in Go, provides a browser-based user interface to
  everything related to BitWrk. The daemon enables control of ongoing trades, registered workers
  and automatic trading mandates. It also provides access to BitWrk's Bitcoin-based payment system.
- The client accepts tasks from BitWrk-enabled programs (such as Blender with the
  BitWrk add-on installed) and dispatches them to the BitWrk service, where they are processed by
  other participants. It also manages local worker programs (such as blender_slave.py) and offers
  their services to the BitWrk exchange for money.

### Build status
master: [![Build Status](https://travis-ci.org/indyjo/bitwrk.svg?branch=master)](https://travis-ci.org/indyjo/bitwrk)
| experimental: [![Build Status](https://travis-ci.org/indyjo/bitwrk.svg?branch=experimental)](https://travis-ci.org/indyjo/bitwrk)

----

|  | Donation Address |
| --- | --- |
| ♥ __BTC__ | 1Lw2kh9WzCActXSGHxyypGLkqQZfxDpw8v |
| ♥ __ETH__ | 0xaBd66CF90898517573f19184b3297d651f7b90bf |
