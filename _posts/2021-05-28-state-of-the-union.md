---
layout: post
title:  "State of the Union"
date:   2021-05-28 16:45:00 +0100
categories: introduction
author:
- Alexandra Settle, Volker Theile, and Alex Lau
---

Where are we at?

Aquarium has made some good progress in the past few weeks. Here are the
following recent highlights:

- We now have a [feature-based development roadmap](https://github.com/aquarist-labs/aquarium/blob/main/doc/project-plan/roadmap.rst)
- We refactored the installer: Now it uses the wizard style in both
  scenarios (setting up new node and adding one to an existing cluster)
- We have 48 GitHub stars and over 67,000 lines of code
- Our website has had a facelift and we now store our meeting minutes
  openly.

Overall, we're in a really good place for Aquarium. Glass is based on Google's
Angular & Angular Material framework. The entire code is written in TypeScript
which is transpiled into JavaScript to be able to run on various browsers.
We decided to only support browsers that support ECMAScript 2015 (ES6), see
[Can I  use ___?](https://caniuse.com/es6).

I have attached a series of screenshots detailing our recent updates to the
installer. These images detail the addition of our new `create` wizard and
relocates a series of components.

The entry point of the Glass UI contains various widgets that support the
administrator to have a quick overview of what is going on the system and
how the status is. As of milestone 4, the user can rearrange and resize the
widgets on their own thanks to the angular-gridster2 library we are using.
For later milestones, we have planned to switch to a fixed layout because
this allows us to have more control of the dashboard related to its size
and the order of the widgets. One of the special features we're working on
is a WebUI layout mapping to help record and identify the hard drive physical
location and virtual OSD mapping. This allows the user to see the data and
drive relationship in the future or maintenance.

The UI already supports internationalization, the translation is done in a
collaborative manner via [transifex](https://www.transifex.com/aquarist-labs/aquarium).
We support English, German, Chinese and Taiwanese.

Gravel, as you know, is a system service, running from an in-memory openSUSE
Tumbleweed image. At the moment, the project only provides Vagrant images, but
already has support for OEM images that can be booted from a USB stick. We have
created a cross-distribution build setup to create a live ISO including Ubuntu
and Debian. This allows any developer to run vagrants with libvirt and
VirtualBox and removes the dependencies for MicroOS.

For our testing setup, we have created wasser. Wasser is a tiny tool for CI/CD
for deployment and test automation. We're also working on a series of
End-to-End (E2E) tests and working on a fully coordinated testing approach.
Alex Lau is working on building out our testing lab in Taiwan. All the cables
received, the memory is ready to go, but he's still waiting on the 10G switch
(which has been delayed due to the latest lockdown). Once the lockdown is over,
Alex will go set them up in the lab.
