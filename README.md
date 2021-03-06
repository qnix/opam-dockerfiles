This repository contains a set of [Docker](http://docker.com) container definitions for various combination of [OCaml](https://ocaml.org) and the [OPAM](https://opam.ocaml.org) package manager.  The containers all come preinstalled with a working compiler and an OPAM environment.  Using it as simple as:

```
docker pull ocaml/opam
docker run -ti ocaml/opam bash
```

...to get a working development environment.  You can grab a specific distribution and test out external dependencies as well:
```
docker run ocaml/opam:ubuntu-16.04_ocaml-4.04.0 opam depext -i cohttp lwt ssl
```

Distributions
==========

The default `latest` tag points to the following distribution:

Distribution | Available Switches | Command
------------ | ------------------ | -------
Debian | 4.02.3 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam`

The latest stable distributions are summarised below.  The default OCaml version available in the container is marked with a &#127347; symbol, and a system installation of OCaml (as opposed to a locally compiled switch) is marked with a &#127362; symbol.

Distribution | Available Switches | Command
------------ | ------------------ | -------
Alpine | 4.04.1 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:alpine`
CentOS | 4.01.0 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:centos`
Debian | 4.02.3 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:debian`
Fedora | 4.02.3 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:fedora`
OpenSUSE | 4.03.0 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:opensuse`
OracleLinux | 4.04.2 &#127347; | `docker pull ocaml/opam:oraclelinux`
Ubuntu | 4.02.3 &#127362;, 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu`

There are also individual containers available for each combination
   of an OS distribution and an OCaml revision. These should be useful for
   testing and continuous integration, since they will remain pinned to these
   versions for as long as the upstream distribution is supported.  Note that
   older releases may have security issues if upstream stops maintaining them.

Distro | Compiler | Command
------ | -------- | -------
Alpine 3.3 | 4.00.1 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.00.1`
Alpine 3.3 | 4.01.0 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.01.0`
Alpine 3.3 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.02.3`
Alpine 3.3 | 4.03.0 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.03.0`
Alpine 3.3 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.03.0_flambda`
Alpine 3.3 | 4.04.0 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.04.0`
Alpine 3.3 | 4.04.1 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.04.1`
Alpine 3.3 | 4.04.2 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.04.2`
Alpine 3.3 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.04.2_flambda`
Alpine 3.3 | 4.05.0 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.05.0`
Alpine 3.3 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.05.0_flambda`
Alpine 3.3 | 4.06.0 &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.06.0`
Alpine 3.3 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.3_ocaml-4.06.0_flambda`
Alpine 3.4 | 4.00.1 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.00.1`
Alpine 3.4 | 4.01.0 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.01.0`
Alpine 3.4 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.02.3`
Alpine 3.4 | 4.03.0 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.03.0`
Alpine 3.4 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.03.0_flambda`
Alpine 3.4 | 4.04.0 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.04.0`
Alpine 3.4 | 4.04.1 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.04.1`
Alpine 3.4 | 4.04.2 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.04.2`
Alpine 3.4 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.04.2_flambda`
Alpine 3.4 | 4.05.0 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.05.0`
Alpine 3.4 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.05.0_flambda`
Alpine 3.4 | 4.06.0 &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.06.0`
Alpine 3.4 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.4_ocaml-4.06.0_flambda`
Alpine 3.5 | 4.00.1 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.00.1`
Alpine 3.5 | 4.01.0 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.01.0`
Alpine 3.5 | 4.02.3 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.02.3`
Alpine 3.5 | 4.03.0 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.03.0`
Alpine 3.5 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.03.0_flambda`
Alpine 3.5 | 4.04.0 &#127362;&#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.04.0`
Alpine 3.5 | 4.04.1 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.04.1`
Alpine 3.5 | 4.04.2 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.04.2`
Alpine 3.5 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.04.2_flambda`
Alpine 3.5 | 4.05.0 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.05.0`
Alpine 3.5 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.05.0_flambda`
Alpine 3.5 | 4.06.0 &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.06.0`
Alpine 3.5 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.5_ocaml-4.06.0_flambda`
Alpine 3.6 | 4.00.1 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.00.1`
Alpine 3.6 | 4.01.0 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.01.0`
Alpine 3.6 | 4.02.3 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.02.3`
Alpine 3.6 | 4.03.0 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.03.0`
Alpine 3.6 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.03.0_flambda`
Alpine 3.6 | 4.04.0 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.04.0`
Alpine 3.6 | 4.04.1 &#127362;&#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.04.1`
Alpine 3.6 | 4.04.2 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.04.2`
Alpine 3.6 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.04.2_flambda`
Alpine 3.6 | 4.05.0 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.05.0`
Alpine 3.6 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.05.0_flambda`
Alpine 3.6 | 4.06.0 &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.06.0`
Alpine 3.6 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:alpine-3.6_ocaml-4.06.0_flambda`
Alpine Stable (3.6) | 4.00.1 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.00.1`
Alpine Stable (3.6) | 4.01.0 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.01.0`
Alpine Stable (3.6) | 4.02.3 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.02.3`
Alpine Stable (3.6) | 4.03.0 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.03.0`
Alpine Stable (3.6) | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.03.0_flambda`
Alpine Stable (3.6) | 4.04.0 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.04.0`
Alpine Stable (3.6) | 4.04.1 &#127362;&#127347; | `docker pull ocaml/opam:alpine_ocaml-4.04.1`
Alpine Stable (3.6) | 4.04.2 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.04.2`
Alpine Stable (3.6) | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.04.2_flambda`
Alpine Stable (3.6) | 4.05.0 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.05.0`
Alpine Stable (3.6) | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.05.0_flambda`
Alpine Stable (3.6) | 4.06.0 &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.06.0`
Alpine Stable (3.6) | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:alpine_ocaml-4.06.0_flambda`
CentOS 6 | 4.00.1 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.00.1`
CentOS 6 | 4.01.0 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.01.0`
CentOS 6 | 4.02.3 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.02.3`
CentOS 6 | 4.03.0 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.03.0`
CentOS 6 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.03.0_flambda`
CentOS 6 | 4.04.0 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.04.0`
CentOS 6 | 4.04.1 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.04.1`
CentOS 6 | 4.04.2 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.04.2`
CentOS 6 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.04.2_flambda`
CentOS 6 | 4.05.0 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.05.0`
CentOS 6 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.05.0_flambda`
CentOS 6 | 4.06.0 &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.06.0`
CentOS 6 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:centos-6_ocaml-4.06.0_flambda`
CentOS 7 | 4.00.1 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.00.1`
CentOS 7 | 4.01.0 &#127362;&#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.01.0`
CentOS 7 | 4.02.3 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.02.3`
CentOS 7 | 4.03.0 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.03.0`
CentOS 7 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.03.0_flambda`
CentOS 7 | 4.04.0 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.04.0`
CentOS 7 | 4.04.1 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.04.1`
CentOS 7 | 4.04.2 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.04.2`
CentOS 7 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.04.2_flambda`
CentOS 7 | 4.05.0 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.05.0`
CentOS 7 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.05.0_flambda`
CentOS 7 | 4.06.0 &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.06.0`
CentOS 7 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:centos-7_ocaml-4.06.0_flambda`
Debian 7 (Wheezy) | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.00.1`
Debian 7 (Wheezy) | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.01.0`
Debian 7 (Wheezy) | 4.02.3 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.02.3`
Debian 7 (Wheezy) | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.03.0`
Debian 7 (Wheezy) | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.03.0_flambda`
Debian 7 (Wheezy) | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.04.0`
Debian 7 (Wheezy) | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.04.1`
Debian 7 (Wheezy) | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.04.2`
Debian 7 (Wheezy) | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.04.2_flambda`
Debian 7 (Wheezy) | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.05.0`
Debian 7 (Wheezy) | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.05.0_flambda`
Debian 7 (Wheezy) | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.06.0`
Debian 7 (Wheezy) | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-7_ocaml-4.06.0_flambda`
Debian 8 (Jessie) | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.00.1`
Debian 8 (Jessie) | 4.01.0 &#127362;&#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.01.0`
Debian 8 (Jessie) | 4.02.3 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.02.3`
Debian 8 (Jessie) | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.03.0`
Debian 8 (Jessie) | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.03.0_flambda`
Debian 8 (Jessie) | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.04.0`
Debian 8 (Jessie) | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.04.1`
Debian 8 (Jessie) | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.04.2`
Debian 8 (Jessie) | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.04.2_flambda`
Debian 8 (Jessie) | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.05.0`
Debian 8 (Jessie) | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.05.0_flambda`
Debian 8 (Jessie) | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.06.0`
Debian 8 (Jessie) | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-8_ocaml-4.06.0_flambda`
Debian 9 (Buster) | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.00.1`
Debian 9 (Buster) | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.01.0`
Debian 9 (Buster) | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.02.3`
Debian 9 (Buster) | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.03.0`
Debian 9 (Buster) | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.03.0_flambda`
Debian 9 (Buster) | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.04.0`
Debian 9 (Buster) | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.04.1`
Debian 9 (Buster) | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.04.2`
Debian 9 (Buster) | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.04.2_flambda`
Debian 9 (Buster) | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.05.0`
Debian 9 (Buster) | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.05.0_flambda`
Debian 9 (Buster) | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.06.0`
Debian 9 (Buster) | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-10_ocaml-4.06.0_flambda`
Debian 9 (Stretch) | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.00.1`
Debian 9 (Stretch) | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.01.0`
Debian 9 (Stretch) | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.02.3`
Debian 9 (Stretch) | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.03.0`
Debian 9 (Stretch) | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.03.0_flambda`
Debian 9 (Stretch) | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.04.0`
Debian 9 (Stretch) | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.04.1`
Debian 9 (Stretch) | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.04.2`
Debian 9 (Stretch) | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.04.2_flambda`
Debian 9 (Stretch) | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.05.0`
Debian 9 (Stretch) | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.05.0_flambda`
Debian 9 (Stretch) | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.06.0`
Debian 9 (Stretch) | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-9_ocaml-4.06.0_flambda`
Debian Stable | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.00.1`
Debian Stable | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.01.0`
Debian Stable | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.02.3`
Debian Stable | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.03.0`
Debian Stable | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.03.0_flambda`
Debian Stable | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.04.0`
Debian Stable | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.04.1`
Debian Stable | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.04.2`
Debian Stable | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.04.2_flambda`
Debian Stable | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.05.0`
Debian Stable | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.05.0_flambda`
Debian Stable | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.06.0`
Debian Stable | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-stable_ocaml-4.06.0_flambda`
Debian Testing | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.00.1`
Debian Testing | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.01.0`
Debian Testing | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.02.3`
Debian Testing | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.03.0`
Debian Testing | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.03.0_flambda`
Debian Testing | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.04.0`
Debian Testing | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.04.1`
Debian Testing | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.04.2`
Debian Testing | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.04.2_flambda`
Debian Testing | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.05.0`
Debian Testing | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.05.0_flambda`
Debian Testing | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.06.0`
Debian Testing | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-testing_ocaml-4.06.0_flambda`
Debian Unstable | 4.00.1 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.00.1`
Debian Unstable | 4.01.0 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.01.0`
Debian Unstable | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.02.3`
Debian Unstable | 4.03.0 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.03.0`
Debian Unstable | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.03.0_flambda`
Debian Unstable | 4.04.0 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.04.0`
Debian Unstable | 4.04.1 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.04.1`
Debian Unstable | 4.04.2 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.04.2`
Debian Unstable | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.04.2_flambda`
Debian Unstable | 4.05.0 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.05.0`
Debian Unstable | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.05.0_flambda`
Debian Unstable | 4.06.0 &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.06.0`
Debian Unstable | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:debian-unstable_ocaml-4.06.0_flambda`
Fedora 22 | 4.00.1 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.00.1`
Fedora 22 | 4.01.0 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.01.0`
Fedora 22 | 4.02.3 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.02.3`
Fedora 22 | 4.03.0 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.03.0`
Fedora 22 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.03.0_flambda`
Fedora 22 | 4.04.0 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.04.0`
Fedora 22 | 4.04.1 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.04.1`
Fedora 22 | 4.04.2 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.04.2`
Fedora 22 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.04.2_flambda`
Fedora 22 | 4.05.0 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.05.0`
Fedora 22 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.05.0_flambda`
Fedora 22 | 4.06.0 &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.06.0`
Fedora 22 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:fedora-22_ocaml-4.06.0_flambda`
Fedora 23 | 4.00.1 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.00.1`
Fedora 23 | 4.01.0 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.01.0`
Fedora 23 | 4.02.3 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.02.3`
Fedora 23 | 4.03.0 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.03.0`
Fedora 23 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.03.0_flambda`
Fedora 23 | 4.04.0 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.04.0`
Fedora 23 | 4.04.1 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.04.1`
Fedora 23 | 4.04.2 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.04.2`
Fedora 23 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.04.2_flambda`
Fedora 23 | 4.05.0 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.05.0`
Fedora 23 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.05.0_flambda`
Fedora 23 | 4.06.0 &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.06.0`
Fedora 23 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:fedora-23_ocaml-4.06.0_flambda`
Fedora 24 | 4.00.1 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.00.1`
Fedora 24 | 4.01.0 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.01.0`
Fedora 24 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.02.3`
Fedora 24 | 4.03.0 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.03.0`
Fedora 24 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.03.0_flambda`
Fedora 24 | 4.04.0 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.04.0`
Fedora 24 | 4.04.1 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.04.1`
Fedora 24 | 4.04.2 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.04.2`
Fedora 24 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.04.2_flambda`
Fedora 24 | 4.05.0 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.05.0`
Fedora 24 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.05.0_flambda`
Fedora 24 | 4.06.0 &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.06.0`
Fedora 24 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:fedora-24_ocaml-4.06.0_flambda`
Fedora 25 | 4.00.1 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.00.1`
Fedora 25 | 4.01.0 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.01.0`
Fedora 25 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.02.3`
Fedora 25 | 4.03.0 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.03.0`
Fedora 25 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.03.0_flambda`
Fedora 25 | 4.04.0 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.04.0`
Fedora 25 | 4.04.1 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.04.1`
Fedora 25 | 4.04.2 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.04.2`
Fedora 25 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.04.2_flambda`
Fedora 25 | 4.05.0 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.05.0`
Fedora 25 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.05.0_flambda`
Fedora 25 | 4.06.0 &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.06.0`
Fedora 25 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:fedora-25_ocaml-4.06.0_flambda`
OpenSUSE 42.1 | 4.00.1 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.00.1`
OpenSUSE 42.1 | 4.01.0 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.01.0`
OpenSUSE 42.1 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.02.3`
OpenSUSE 42.1 | 4.03.0 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.03.0`
OpenSUSE 42.1 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.03.0_flambda`
OpenSUSE 42.1 | 4.04.0 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.04.0`
OpenSUSE 42.1 | 4.04.1 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.04.1`
OpenSUSE 42.1 | 4.04.2 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.04.2`
OpenSUSE 42.1 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.04.2_flambda`
OpenSUSE 42.1 | 4.05.0 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.05.0`
OpenSUSE 42.1 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.05.0_flambda`
OpenSUSE 42.1 | 4.06.0 &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.06.0`
OpenSUSE 42.1 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.1_ocaml-4.06.0_flambda`
OpenSUSE 42.2 | 4.00.1 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.00.1`
OpenSUSE 42.2 | 4.01.0 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.01.0`
OpenSUSE 42.2 | 4.02.3 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.02.3`
OpenSUSE 42.2 | 4.03.0 &#127362;&#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.03.0`
OpenSUSE 42.2 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.03.0_flambda`
OpenSUSE 42.2 | 4.04.0 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.04.0`
OpenSUSE 42.2 | 4.04.1 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.04.1`
OpenSUSE 42.2 | 4.04.2 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.04.2`
OpenSUSE 42.2 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.04.2_flambda`
OpenSUSE 42.2 | 4.05.0 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.05.0`
OpenSUSE 42.2 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.05.0_flambda`
OpenSUSE 42.2 | 4.06.0 &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.06.0`
OpenSUSE 42.2 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:opensuse-42.2_ocaml-4.06.0_flambda`
OracleLinux 7 | 4.00.1 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.00.1`
OracleLinux 7 | 4.01.0 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.01.0`
OracleLinux 7 | 4.02.3 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.02.3`
OracleLinux 7 | 4.03.0 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.03.0`
OracleLinux 7 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.03.0_flambda`
OracleLinux 7 | 4.04.0 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.04.0`
OracleLinux 7 | 4.04.1 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.04.1`
OracleLinux 7 | 4.04.2 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.04.2`
OracleLinux 7 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.04.2_flambda`
OracleLinux 7 | 4.05.0 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.05.0`
OracleLinux 7 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.05.0_flambda`
OracleLinux 7 | 4.06.0 &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.06.0`
OracleLinux 7 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:oraclelinux-7_ocaml-4.06.0_flambda`
Ubuntu 12.04 | 4.00.1 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.00.1`
Ubuntu 12.04 | 4.01.0 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.01.0`
Ubuntu 12.04 | 4.02.3 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.02.3`
Ubuntu 12.04 | 4.03.0 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.03.0`
Ubuntu 12.04 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.03.0_flambda`
Ubuntu 12.04 | 4.04.0 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.04.0`
Ubuntu 12.04 | 4.04.1 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.04.1`
Ubuntu 12.04 | 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.04.2`
Ubuntu 12.04 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.04.2_flambda`
Ubuntu 12.04 | 4.05.0 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.05.0`
Ubuntu 12.04 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.05.0_flambda`
Ubuntu 12.04 | 4.06.0 &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.06.0`
Ubuntu 12.04 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-12.04_ocaml-4.06.0_flambda`
Ubuntu 14.04 | 4.00.1 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.00.1`
Ubuntu 14.04 | 4.01.0 &#127362;&#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.01.0`
Ubuntu 14.04 | 4.02.3 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.02.3`
Ubuntu 14.04 | 4.03.0 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.03.0`
Ubuntu 14.04 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.03.0_flambda`
Ubuntu 14.04 | 4.04.0 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.04.0`
Ubuntu 14.04 | 4.04.1 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.04.1`
Ubuntu 14.04 | 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.04.2`
Ubuntu 14.04 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.04.2_flambda`
Ubuntu 14.04 | 4.05.0 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.05.0`
Ubuntu 14.04 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.05.0_flambda`
Ubuntu 14.04 | 4.06.0 &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.06.0`
Ubuntu 14.04 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-14.04_ocaml-4.06.0_flambda`
Ubuntu 16.04 | 4.00.1 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.00.1`
Ubuntu 16.04 | 4.01.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.01.0`
Ubuntu 16.04 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.02.3`
Ubuntu 16.04 | 4.03.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.03.0`
Ubuntu 16.04 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.03.0_flambda`
Ubuntu 16.04 | 4.04.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.04.0`
Ubuntu 16.04 | 4.04.1 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.04.1`
Ubuntu 16.04 | 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.04.2`
Ubuntu 16.04 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.04.2_flambda`
Ubuntu 16.04 | 4.05.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.05.0`
Ubuntu 16.04 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.05.0_flambda`
Ubuntu 16.04 | 4.06.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.06.0`
Ubuntu 16.04 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.04_ocaml-4.06.0_flambda`
Ubuntu 16.10 | 4.00.1 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.00.1`
Ubuntu 16.10 | 4.01.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.01.0`
Ubuntu 16.10 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.02.3`
Ubuntu 16.10 | 4.03.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.03.0`
Ubuntu 16.10 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.03.0_flambda`
Ubuntu 16.10 | 4.04.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.04.0`
Ubuntu 16.10 | 4.04.1 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.04.1`
Ubuntu 16.10 | 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.04.2`
Ubuntu 16.10 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.04.2_flambda`
Ubuntu 16.10 | 4.05.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.05.0`
Ubuntu 16.10 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.05.0_flambda`
Ubuntu 16.10 | 4.06.0 &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.06.0`
Ubuntu 16.10 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-16.10_ocaml-4.06.0_flambda`
Ubuntu 17.04 | 4.00.1 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.00.1`
Ubuntu 17.04 | 4.01.0 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.01.0`
Ubuntu 17.04 | 4.02.3 &#127362;&#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.02.3`
Ubuntu 17.04 | 4.03.0 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.03.0`
Ubuntu 17.04 | 4.03.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.03.0_flambda`
Ubuntu 17.04 | 4.04.0 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.04.0`
Ubuntu 17.04 | 4.04.1 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.04.1`
Ubuntu 17.04 | 4.04.2 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.04.2`
Ubuntu 17.04 | 4.04.2+flambda &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.04.2_flambda`
Ubuntu 17.04 | 4.05.0 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.05.0`
Ubuntu 17.04 | 4.05.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.05.0_flambda`
Ubuntu 17.04 | 4.06.0 &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.06.0`
Ubuntu 17.04 | 4.06.0+flambda &#127347; | `docker pull ocaml/opam:ubuntu-17.04_ocaml-4.06.0_flambda`


Using the Containers
================

Each container comes with an initialised OPAM repository pointing to the central repository. The default user in the container is called `opam`, and `sudo` is configured to allow password-less access to `root`.

To build an environment for the [Jane Street Core](https://realworldocaml.org/) library on the latest stable OCaml, a simple Dockerfile looks like this:

```
FROM ocaml/opam
RUN opam depext -i core
```
You can build and use this image locally for development by saving the Dockerfile and:

```
docker build -t ocaml-core .
docker run -ti ocaml-core bash
```

You can also use the Docker [volume sharing](https://docs.docker.com/engine/reference/builder/#volume) to map in source code from your host into the container to persist the results of your build.  You can also construct more specific Dockerfiles that use the full range of OPAM commands for a custom development environment.  For example, to build the [MirageOS](https://mirage.io) bleeding edge OCaml environment, this Dockerfile will add in a custom remote:

```
FROM ocaml/opam:ubuntu-15.10_ocaml-4.02.3
RUN opam remote add dev git://github.com/mirage/mirage-dev
RUN opam depext -i mirage
```



Contributing
==========

To discuss these containers, please e-mail Anil Madhavapeddy <anil@recoil.org> or the OPAM development list at <opam-devel@lists.ocaml.org>. Contributions of Dockerfiles for additional OS distributions are most welcome! The files here are all autogenerated from the [ocaml-docker-scripts](https://github.com/avsm/ocaml-docker-scripts) repository, so please do not submit any PRs directly to this location. The containers are built and hosted on the Docker Hub [ocaml organisation](https://hub.docker.com/u/ocaml).
