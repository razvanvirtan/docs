+++
title = "Unikraft: Building Powerful Unikernels Has Never Been Easier!"
date = "2020-02-17T00:00:00+01:00"
tags = ["release"]
+++

Two years ago, the Xen Project introduced
[Unikraft](http://unikraft.org) as an incubation project. Over the
past two years, the Unikraft project has seen some great
momentum. Since the last release, the community has grown about 20%
and contributions have diversified a great deal. Contributions from
outside the project founders (NEC) now make up 63% of all
contributions, up from about 25% this time last year! In addition, a
total of 56739 lines were added since the last release (0.3).

As a quick primer, Unikraft provides an easier way to build
unikernels, compiling source code into a lean operating system that
includes functionality specifically tailored to the needs of the
application logic. Unikernels, being ultra-lightweight and small, are
ideal for not just cloud applications (Unikraft supports deployment on
AWS, GCP and Digital Ocean) but also for fields where resources may be
constrained or safety is critical. In fact, Unikraft is not only able
to produce extremely efficient virtual machines, but in ongoing work
also specialized OCI/Docker containers and even bare metal ARM64
images ideally suited for IoT and embedded devices. On a Raspberry Pi
3 B+, for example, Unikraft is able to boot in under 10 milliseconds.

Over the past two years, the Unikraft team has made great progress in
simplifying the process of building unikernels through a unified and
customizable code base. Unikraft has seen a major increase in features
and functionality since the last release. Some of the notable
additions for this release (`0.4 Rhea`) are:

* Cloud-based deployments (GCP, AWS, Digital Ocean)
* Native support for many programming languages and language environments: C++, Python/Micropython, Go, Lua, Web Assembly (WAMR), JavaScript (Duktape), Ruby
* Improvements to the ARM64 platform, including virtio and multi-thread support
* Basic musl support
* pthread and TLS support
* Trace point sub-system
* Filesystem support (9pfs, devfs, ramfs)
* Applications: Click, SQLite, nginx, redis
* Support for external platforms, and in particular solo5
* Additional lib ports: uuid, http-parser, intel-intrinsics, openssl, boost, protobuf, etc.
* Lots of other features and bug fixes

In addition, with this release we’re introducing the `kraft` tool which
greatly simplifies the process of building and running Unikraft-built
unikernels; check it out [here](https://github.com/unikraft/kraft) (a
special thank you goes to Alexander Jung and Mujahid Ali for creating this
tool).

As with every release, we are extremely grateful to those who
contributed and continue to contribute to this project; below are the
contributors (based on Signed-off-by tags):

```
Costin Lupu                     270 (22.0%)
Vlad-Andrei BĂDOIU (78692)      155 (12.7%)
Simon Kuenzer                   127 (10.4%)
Felipe Huici                     98 (8.0%)
Yuri Volchkov                    75 (6.1%)
Sharan Santhanam                 74 (6.0%)
Florian Schmidt                  69 (5.6%)
Jia He                           60 (4.9%)
Wei Chen                         45 (3.7%)
Mihai Pogonaru                   37 (3.0%)
Gaulthier Gain                   36 (2.9%)
Cristian Banu                    31 (2.5%)
Charalampos Mainas               29 (2.4%)
Roxana Nicolescu                 28 (2.3%)
Jianyong Wu                      15 (1.2%)
Andrei Gogonea                   12 (1.0%)
Hugo Lefeuvre                    11 (0.9%)
Bogdan Lascu                     10 (0.8%)
Teodora Serbanescu                8 (0.7%)
Stefan Teodorescu                 8 (0.7%)
Santiago Pagani                   8 (0.7%)
Alexander Jung                    7 (0.6%)
Haibo Xu                          7 (0.6%)
```

In addition, we would like to thank all of the reviewers who spent
significant amounts of time upstreaming code to Unikraft:

```
Felipe Huici                    356 (33.3%)
Costin Lupu                     189 (17.7%)
Simon Kuenzer                   158 (14.8%)
Sharan Santhanam                 90 (8.4%)
Vlad-Andrei BĂDOIU (78692)       61 (5.7%)
Florian Schmidt                  56 (5.2%)
Stefan Teodorescu                39 (3.6%)
Roxana Nicolescu                 27 (2.5%)
Gaulthier Gain                   24 (2.2%)
Santiago Pagani                  19 (1.8%)
Charalampos Mainas               17 (1.6%)
Yuri Volchkov                    13 (1.2%)
Jia He                           11 (1.0%)
Mihai Pogonaru                    5 (0.5%)
Alexander Jung                    3 (0.3%)
Julien Grall                      1 (0.1%)
```

Beyond the features of this `0.4 Rhea` release, we are excited to give
you a sneak peak into the features that are likely to make it into the
next release:

* Additional external platform support (e.g., Amazon Firecracker)
* Bare metal support (ARM64/Raspberry Pi and others)
* OCI/Docker support: have Unikraft generate extremely specialized containers
* Binary compatibility: run unmodified Linux ELFs directly on Unikraft

Finally, the Unikraft team's Simon Kuenzer recently gave a talk at
FOSDEM titled [Unikraft: A Unikernel Toolkit](https://fosdem.org/2020/schedule/event/uk_unicraft/). Simon, a senior systems
researcher at NEC Labs and the lead maintainer of Unikraft, spoke all
about Unikraft and provided a comprehensive overview of the project,
where it’s been and what’s in store.
