---
layout: post
title: MyBB 1.8.16 Released - Security & Maintenance Release
date: 2018-07-04 18:08 -05:00
categories:
- Releases
- Security
- Updates
tags: []
author: Devilshakerz
---
MyBB 1.8.16 is now available, and is a security &amp; maintenance release.

This update includes compatibility fixes for database engines and recent PHP versions as well as performance and global security improvements. Note that the theme’s CSS files may need to be updated. If you use the *login_attempt_check()* function, note that [its signature has changed](https://github.com/mybb/mybb/pull/3115#discussion_r192568912).

- **6 security vulnerabilities addressed:**
  - High risk: Image &amp; URL MyCode Persistent XSS — reported by [Punisher_HF](https://community.mybb.com/user-121288.html)
  - Medium risk: Multipage Reflected XSS — reported by Dimaz Arno of Ethic Ninja
  - Low risk: ACP logs XSS — reported by [Cillian Collins](https://github.com/Cillian-Collins)
  - Low risk: Arbitrary file deletion via ACP's Settings — reported by [Devilshakerz](https://community.mybb.com/user-47371.html) of MyBB Team
  - Low risk: Login CSRF — reported by [Cillian Collins](https://github.com/Cillian-Collins)
  - Low risk: Non-video content embedding via Video MyCode — reported by [Punisher_HF](https://community.mybb.com/user-121288.html)
- **[66 issues resolved](https://github.com/mybb/mybb/issues?q=is%3Aissue%20is%3Aclosed%20label%3As%3Afixed%20milestone%3A1.8.16)**

Check **[Release Notes](https://mybb.com/versions/1.8.16/)** for a list of changes to language files, templates and unresolved issues.

## Issues on Upgrade?

- **[SQL syntax error during upgrade](https://github.com/mybb/mybb/issues/3312)**: overwrite *[install/resources/upgrade43.php](https://raw.githubusercontent.com/mybb/mybb/a0ee7fb1774dc23c34924078d8c434c99146e36a/install/resources/upgrade43.php)* and run the upgrade process again
- **["not allowed" reporting problem](https://github.com/mybb/mybb/issues/3306)**: overwrite *[report.php](https://raw.githubusercontent.com/mybb/mybb/6eb3cb6ba31aa9a9160e8a754e07efa9441c306b/report.php)*
- **"Authorization code mismatch" on login**: use the ACP's *Find Updated Templates* feature to insert missing `my_post_key` input fields to login forms ([more information](https://community.mybb.com/thread-218460-post-1308277.html#pid1308277))

<a href="https://mybb.com/download" class="button button--medium">{% include icon.html icon='download' %} Get MyBB</a> <a href="https://mybb.com/versions/1.8.16/" class="button button--medium button--secondary">{% include icon.html icon='info-circle' %} Release Notes</a>

The MyBB Project extends thanks to reporters and researchers following responsible disclosure.

Go to [mybb.com/security](https://mybb.com/get-involved/security/) to report possible security concerns or to learn more about security research at MyBB. If you would like to contribute to the Project, [Get Involved](https://mybb.com/get-involved/).

Thanks,<br>
MyBB Team
