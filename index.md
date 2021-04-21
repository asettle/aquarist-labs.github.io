---
list_title: "Blogs"
---

![GitHub Repo stars](https://img.shields.io/github/stars/aquarist-labs/aquarium?style=social)

![GitHub last commit](https://img.shields.io/github/last-commit/aquarist-labs/aquarium) ![Lines of code](https://img.shields.io/tokei/lines/github/aquarist-labs/aquarium) ![GitHub contributors](https://img.shields.io/github/contributors/aquarist-labs/aquarium) ![GitHub issues](https://img.shields.io/github/issues/aquarist-labs/aquarium) ![GitHub milestones](https://img.shields.io/github/milestones/all/aquarist-labs/aquarium)


Aquarium is a [SUSE](https://suse.com/)-sponsored Open Source
project to build an easy-to-use, rock-solid appliance wrapped around the
[Ceph](http://ceph.io) project. The project started development in January 2021,
and has become a passion project for the storage team at SUSE.

We are investigating the beginnings of a new storage appliance project in
an opinionated fashion. The Aquarium project is split into two clearly
defined work streams: Gravel (backend) and Glass (frontend).

On this website, you're invited to follow along our experiments on
captive cephalopods in decorative containers! Please see [our license](https://aquarist-labs.github.io/LICENSE)
and [our quickstart guide on how to
contribute](https://aquarist-labs.github.io/docs/dev/contributing-to-the-website.html).

## Who Are We?

We are a collective group of Ceph and storage enthusiasts who are looking to
find ways to simplify the Ceph installer process. We are redefining what it
means to create a storage appliance, while keeping to the basics of building
something that can provide and manage data without an application context.

## Our Mission

Currently, we see Ceph as being too complex to use for the average user. This
complexity stems from Ceph's flexibility that supports a huge matrix of use
cases and the effects this has on available capacity, performance and thus
availability.

All current management tooling deploys Ceph bottom-up, i.e. the user must
specify deployment patterns at the daemon level, create pools and crushmaps
(which encode various availability and performance requirements) and only then
can a user deploy their workload.

We are exploring if other user interface abstractions are practical and
ultimately an improvement. The goal should be simplification where a user is
not required to configure individual daemons or disk layouts, but can provide
a high level specification of what they want (in terms of availability, usable
capacity, ...?) and a piece of code translates that to a deployment layout.
Whether this deployment layout can be set up on the current hardware can be
determined by software and the user can be provided with the feedback (be it
positive or negative).

![Aquarium Logo](/images/squido-v2.svg)
