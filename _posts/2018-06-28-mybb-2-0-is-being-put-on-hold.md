---
layout: post
title: MyBB 2.0 is being put on hold
date: 2018-06-28 20:01 -05:00
categories:
- Uncategorized
tags: []
author: andrewjs18
---

The community spoke and we are listening.

Effective immediately, the MyBB team will be putting 2.0 on hold and working towards a more viable &amp; gradual approach to rewriting the core software. Rather than a total rewrite all at once that could take years to complete, we're going to roll out smaller updates in a quicker fashion. Starting with MyBB 1.9 and onwards, each release (1.10, 1.11, 1.12, etc.) will have new features and rewritten code until we reach the ultimate goal of a totally rewritten and modern forum software.

First up is MyBB 1.9. This update will feature a [responsive theme](https://web.archive.org/web/20180627194402/http://mybb.jsoltesz.com/mybb-theme/) built on a new and improved, [Twig](https://twig.symfony.com/) template system. This system will allow template conditionals, variable loops, template includes, and much more. Along with a new theme and template system, we're reworking &amp; improving all of the javascript code and moving it from being inline with the theme to external files. Doing this will make it easier to manage and allow site owners to more easily implement better [Content Security Policies](https://developer.mozilla.org/en-US/docs/Web/HTTP/CSP) on their forum.

In addition to the theme work outlined above, we're going to be replacing SCEditor with [TinyMCE](https://www.tinymce.com/) as well as introducing the [Swiftmailer](https://swiftmailer.symfony.com/) mail handler. TinyMCE should be a vast improvement to the overall user experience compared to the current editor we're using in the 1.8 series. TinyMCE is well-supported &amp; maintained, modern and easily extensible with plugins if you're looking for extra functionality. Swiftmailer will improve our core email functionality and should integrate better with most SMTP hosts. Swiftmailer will also allow us to retry sending failed emails, add attachments, use the BCC &amp; CC functionality, support servers that require usernames &amp; passwords and/or encryption and much more.

We are excited to embark on this path together with the end goal being to restore MyBB's place as the best forum software available today— free or commercial.

Thank you for you feedback. Please continue to voice your opinion about the things that are important to you. We are all in this together!

Follow the links below to view the MyBB 1.9 repository and MyBB 1.9 forum topic, respectively:

<a href="//github.com/mybb/mybb/tree/develop/1.9" class="button button--medium" title="MyBB 1.9 Repository">{% include icon.html icon='github' %} View on GitHub</a> <a href="//community.mybb.com/thread-215211.html" class="button button--medium button--secondary" title="MyBB 1.9 Forum Topic">{% include icon.html icon='arrow-right' %} Visit Forum</a>
