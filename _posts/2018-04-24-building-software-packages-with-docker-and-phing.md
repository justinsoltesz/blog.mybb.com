---
layout: post
title: Building software packages with Docker and Phing
date: 2018-04-24 13:31 -05:00
categories:
- Development
tags: []
author: Devilshakerz
---

Every meaningful set of [development activity](https://github.com/mybb/mybb/commits/feature) in open-source projects like MyBB is followed by an official [release](https://docs.mybb.com/1.8/development/release-workflow/) that merges in additional lines of production, like security updates, and wraps it up with descriptions and instructions easy to understand for non-developers and site maintainers. Currently the most popular way of distributing updates to PHP-based software is file packages: project managers have to scramble to gather and bundle all files and associated documentation while site administrators are expected to keep track of (and sometimes interpret) this information.

This, to convenience of site administrators and ours, is planned to improve upon adoption of concepts like [continuous integration](https://www.thoughtworks.com/continuous-integration) that put emphasis on making all products deployable after every change to the code, and the integration of tools like [Composer](https://getcomposer.org/), which ease the pains of managing third-party solutions and allow to separate one big product into small, handy modules. Even though conveniences like fully automated updates will take time to become reality with informal open-source projects (where the technicalities are much easier to implement than procedures that provide a reasonable level of security), MyBB moves closer to that with eliminating manual tasks covering a broad range of activities that precede each release—the last 4 versions of MyBB (starting with 1.8.12) have been build using the recently published [**package builder**](https://github.com/mybb/mybb-build).

<a href="https://github.com/mybb/mybb-build" class="button button--medium">{% include icon.html icon='github' %} View on GitHub</a>

### Rewriting Memos in XML &amp; PHP

The core part of the builder's logic is [**Phing**](https://www.phing.info/), an *Apache Ant*-based PHP **task build system**. This engine enables developers to specify operations related i.a. to *git* &amp; *patch* (extensively used to apply sensitive patches before the release), file encoding and archiving saved in an XML [build file](https://github.com/mybb/mybb-build/blob/master/build.xml). It's also used to call sub-scripts that list changed files and calculate archive size and checksums, but also perform some project-specific operations like counting modified language files, searching for templates that changed between versions or update plugin hook locations with line number precision. Since the Jekyll-powered *MyBB.com* website is generated from Markdown &amp; Front Matter data files, the builder also prepares the version's YaML metadata ready to be put [into the repository](https://github.com/mybb/mybb.com/tree/gh-pages/_versions) allowing Release Notes and the Release Blog Post content to be generated.

### You Want to Run it on *What*?

Another important role plays [**Docker**](https://www.docker.com/what-docker), a platform introducing **container systems**. You might recognize it from the recently put out [image recipe](https://blog.mybb.com/2017/11/25/mybb-1-8-dockerfile-docker-compose-recipe/) that can be used to deploy MyBB 1.8, however this environment is also used whenever packages need to be assembled. No matter who, where or when participates in the building process, they should be able to use the same precisely defined tools—by running the script inside a container we can assure a degree of confidence in that, given the separation from the host operating system. Our Docker image, based on a trimmed down version of Debian, contains an unsuspicious development toolset including basic packages and a PHP interpreter with customized configuration and the `strip-nondeterminism` tool that normalizes the output to make it possible to arrive with byte-to-byte equal archives identified by matching checksums. This practice is called *build reproducibility* which will serve as a vital part in download verification.

<a href="{{ site.baseurl }}/assets/images/2018/04/mybb-build-shell.gif" title="Real output (with real git errors) when building MyBB 1.8.15 packages" class="blog-post__image-link"><img src="{{ site.baseurl }}/assets/images/2018/04/mybb-build-shell.gif" alt="Real output (with real git errors) when building MyBB 1.8.15 packages" class="blog-post__image-link__image" /></a>

Visit the [mybb/mybb-build](https://github.com/mybb/mybb-build) repository to set up own production line basing on our code and compare against the latest MyBB release packages (starting with 1.8.15, [releases on GitHub](https://github.com/mybb/mybb/releases) include a build package with input necessary to reproduce the output).

<a href="https://github.com/mybb/mybb-build" class="button button--medium button--secondary">{% include icon.html icon='arrow-right' %} Get Started</a>

Automated packaging does not only leave more time for other aspects of running large-scale projects, but also assures that every update is brought to users without potential mistakes that could have been made otherwise with manual assembling. Furthermore, whenever mistakes are spotted, the archives can be quickly rebuilt and pushed out—less emphasis will be put on singular releases and more on their continuous delivery with seamless upgrades that MyBB will be working on.
