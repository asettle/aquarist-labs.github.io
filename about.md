---
layout: page
title: "About"
permanlink: /ABOUT/
---

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
