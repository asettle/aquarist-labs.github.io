---
layout: page
title: "FAQ"
permanlink: /FAQ/
---

# General
-----------

**Q:** What is Aquarium?

**A:** Aquarium is an open source project investigating the beginnings of a new
storage appliance project in an opinionated fashion.

-----------

**Q:** Who is Aquarist Labs?

**A:** We are a group of like-minded individuals that are passionate about storage,
Ceph, and open development. We are a SUSE-sponsored project looking to further
expand our reach.

-----------

**Q:** Is this an open source project?

**A:** Absolutely! Everything we're doing is in the open: development, discussions,
decision making, even our meetings.

-----------

**Q:** How is this project related to Ceph?

**A:** Being Ceph developers and enthusiasts, we're building Aquarium on top
of Ceph. Providing an appliance style deployment and a service-based GUI, but
it's still Ceph underneath.

-----------

**Q:** How do I get involved?

**A:** Look at the [issue](https://github.com/aquarist-labs/aquarium/issues) list or
check out our Slack channel (see below) and ask one of the friendly contributors.
You can also view our [project board](https://github.com/orgs/aquarist-labs/projects/3)
and check our [Review Guidelines](https://github.com/aquarist-labs/aquarium/blob/main/CONTRIBUTING.md).

If you want to get your hands dirty as soon as possible, you can also run the
script at `tools/setup-dev.sh`. This will ensure you have a basic development
environment as soon as possible so you can start hacking.

You will be able to find the backend bits in `src/gravel`, while the frontend
bits are located in `src/glass`.

Check out our [From Zero to Hacking](https://github.com/aquarist-labs/aquarium/blob/main/doc/from-zero-to-hacking.md)
quickstart to help you get off your feet.

-----------

**Q:** Where can I get more help, if I need it?

**A:** Join us on Slack! You can sign up [here](https://join.slack.com/t/aquaristlabs/shared_invite/zt-lsjrkw8m-Jj_zYAs84PfMsUGwvMDOFA).

We have the following channels:

- #announcements: For all announcements related to Aquarist Labs and the Aquarium project
- #aquarium: For all conversation and questions surrounding the Aquarium project
- #general: Show us your best gif!
- #github-notifications: Notifications from the [github app](https://slack.github.com/).

If you have a new idea, or want to discuss any implementation details, we recommend using our [Discussion page](https://github.com/aquarist-labs/forum/discussions) on GitHub.

-----------

**Q:** What is a storage appliance?

**A:** A storage appliance is something that can provide or manage data without
an application context to add simplification to the day 1 installer experience.
This is often displayed in the form of a wizard-driven installation process, but
it can also mean a fixed hardware configuration.

We're still working on defining what this means for *us*. Stay tuned for more,
or join the [discussion](https://github.com/aquarist-labs/forum/discussions/12).

-----------

**Q:** How does a storage appliance suit my use case?

**A:**

-----------

# Technical


**Q:** Does Aquarium support the same services and features as Ceph?

**A:** We deliberately do not expose all features in order to simplify deployment
and management for what we think are common or useful deployment scenarios.
However, you will recognise 

-----------

**Q:** ...

**A:**
