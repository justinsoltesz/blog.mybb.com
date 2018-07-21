---
layout: post
title: MyBB 1.8.15 Released - Security & Maintenance Release
date: 2018-03-15 19:55 -05:00
categories:
- Releases
- Security
- Updates
tags: []
author: Devilshakerz
---

MyBB 1.8.15 is now available, and is a security &amp; maintenance release.<br><br>

This update includes compatibility improvements for PostgreSQL and recent PHP versions as well as minor optimizations.<br><br>

- **10 security vulnerabilities addressed:**
  - Medium risk: Tasks Local File Inclusion &mdash; reported by [Riley Baird](http://www.batterystapl.es/2018/03/local-file-inclusion-and-reading.html)
  - Medium risk: Forum Password Check Bypass &mdash; reported by [Riley Baird](http://www.batterystapl.es/2018/03/local-file-inclusion-and-reading.html)
  - Low risk: Admin Permissions Group Title XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Attachment types file extension XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Moderator Tools XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Security Questions XSS &mdash; reported by [doylecc](https://community.mybb.com/user-14694.html)
  - Low risk: Settings Management XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Templates Set Name XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Usergroup Promotions XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
  - Low risk: Warning Types XSS &mdash; reported by [Nathaniel Suchy](https://github.com/nsuchy)
 - **[24 issues resolved](https://github.com/mybb/mybb/issues?q=is%3Aissue%20is%3Aclosed%20label%3As%3Afixed%20milestone%3A1.8.15)**

Check **[Release Notes](https://mybb.com/versions/1.8.15/)** for a list of changes to language files, templates and unresolved issues.

<a href="https://mybb.com/download" class="button button--medium">{% include icon.html icon='download' %} Get MyBB</a> <a href="https://mybb.com/versions/1.8.15/" class="button button--medium button--secondary">{% include icon.html icon='info-circle' %} Release Notes</a>

The MyBB Project extends thanks to reporters and researchers following responsible disclosure.

Go to [mybb.com/security](https://mybb.com/get-involved/security/) to report possible security concerns or to learn more about security research at MyBB. If you would like to contribute to the Project, [Get Involved](https://mybb.com/get-involved/).

Thanks,<br>
MyBB Team
