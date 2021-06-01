---
layout: post
title:  "Introducing... Gravel!"
date:   2021-06-01 17:49:00 +0100
categories: introduction
author:
- João Luis
---

Introducing... Gravel!

This series called "Introducing..." highlights a key component, change, or
feature set. This week, we're introducing our backend system: Gravel.

Aquarium is running from an in-memory openSUSE Tumbleweed image. At the moment,
the project only provides Vagrant images on a weekly basis, but we already have
support for OEM images to be built, which can be booted from a USB stick.

By keeping Aquarium as a RAM disk, we are aiming at reducing the overhead of
upgrading the system, detaching the OS and Aquarium's upgrade from the
remaining system. This is rather important because this means that an Aquarium
upgrade can take just as long as it takes to boot a single image, instead of
having to wait for a full system upgrade, minimizing the impact the system's
upgrade might have on cluster availability.

Persistent state that might be needed, including Ceph container images, will
be kept on a system disk that is created, partitioned, and mounted by Gravel
during node deployment -- setup of this system disk is currently work in
progress, and we are expecting to have support in the next week or so.

Upon boot Gravel will be started, being a system service, providing a REST API
to interface with Glass and other Aquarium nodes. Gravel is the brains of the
operation, holding the logic that glues Glass with the rest of the system,
including the underlying Ceph cluster.

Gravel is responsible for setting up a node upon initial deployment, including
its system disk, and the bits that will be required for proper Aquarium
operation: etcd to store distributed persistent state, and Ceph for the
underlying storage system. Both these components will be run from containers
that are initially bundled in the provided image but, at some point, we aim to
allow them to be upgraded according to to-be-defined criteria.

It is also through Gravel that additional nodes will be added to the
cluster, although deployment for a new node roughly follows the same steps as
the first node. At the moment we support adding any number of new nodes,
although we've only tested up to four virtual nodes.

Gravel abstracts certain Ceph concepts, so that Glass can abstract those
concepts for the user. Amongst them we have 'services', which abstract the
concept of pools and Ceph services. At the moment we support a File Service,
with two supported backends (cephfs and NFS), and are in the planning phase of
adding an Object Service (backed by RGW) for Milestone 5. We are planning on
adding a Block Service, backed by RBD and iSCSI, in later milestones.

A lot of recent Gravel work has gone towards stabilization and testing. On top
of having added unit tests on the previous milestone, which are now criteria for
merging new code, we have created a functional test battery that aims at testing
a live cluster, exercising the whole stack. We intend to make this merge
criteria by end of Milestone 5.
