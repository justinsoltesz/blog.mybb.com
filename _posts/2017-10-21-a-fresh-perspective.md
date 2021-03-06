---
layout: post
title: A Fresh Perspective
date: 2017-10-21 15:00:20.000000000 -04:00
categories:
- General
- Updates
author: Eric J.
---
<img src="{{ site.baseurl }}/assets/images/2017/10/17-head.jpg" alt="Blog header image" />

MyBB has been making some changes lately, and if you haven’t noticed we’re here to give you the scoop. Discussion about bridging 1.x closer to 2.0 has been settling, and as such we have decided on the best course of action moving forward. This comes with some other updates, including the main site going responsive, our blog getting way more fun, setting up an official demo site, and speeding up that darn extension approval process.

## MyBB.com

If you’ve browsed our site lately on mobile, you may have noticed that it can be a real pain to navigate. We believe it is time to change that. Rather than awaiting MyBB 2 to bring our website into the modern age, you can expect it to be updated ***very*** soon. The new site will feature a few things:

- Modern Design - *We are making sure to get the site up to modern design standards.*
- Fully Responsive - *This is part of a larger goal to get all MyBB products responsive, we’re starting with the main site.*
- SEO - *Finding pages on MyBB should be a much better experience through search engines.*

If you have some time and want to leave some feedback, or if you just want to look at the new design, please visit the thread or repository linked below. Thanks!

<a href="https://community.mybb.com/thread-213603-post-1286609.html#pid1286609" class="button">{% include icon.html icon='comments' %} Visit Thread </a> <a href="https://github.com/mybb/wip.mybb.com" class="button">{% include icon.html icon='github' %} View on GitHub</a>

## Blog

Our blog will be getting some love as well. We’re now creating our blog posts via a repository on GitHub, so you can help (Or just get a sneak peek at what the next blog will be about). If you have an idea for a blog post that we haven’t done yet, or think we could be doing something better, feel free to open an issue in the repository linked below.

<a href="https://github.com/mybb/blog.mybb.com-drafts" class="button">{% include icon.html icon='github' %} View on GitHub</a>

## Official Demo Site

You may or may not know this, but we keep the community forum as vanilla as possible so users can get a feel for what MyBB is, right out of the box. Unfortunately this limits some decisions we make where improving the community forum is concerned. Not only that, but it limits how users can explore a vanilla MyBB installation as well. We are going to be creating a demo website to solve both of these issues, allowing you as users to browse a clean installation of MyBB easily. Obviously these demo installs will be lacking a couple of features that a full blown install contains, such as the ability to install custom themes and plugins - this is purely a security precaution.

Providing a clean demo system for users also opens up the possibility for more changes to be made to the official community forum - such as updating the styling to fit in with the rest of the website - in the future.

You can expect work to begin on this project after the new website has launched. Stay tuned for further updates!

## MyBB Extensions

### Approval Process

It’s no secret that getting a modification approved on the MyBB website can be a slow process. The main offender for this is our mission to make sure submissions are safe and of good quality, which means exploring the code and installing them for ourselves. This just isn’t a sustainable practice and results in a lot of frustration.

To speed up your addon submissions, we’re going to be easing our policy for allowing submissions. The policy has been published in our documentation, check it out at the following link.

<a href="https://docs.mybb.com/extend/review-process/" class="button">{% include icon.html icon='book' %} View in Docs</a>

If you find an issue with one of these unapproved addons, or even one that has been approved, please report it to us via the Private Inquiries forum so we can investigate properly.

### Paid Modification Support

We are also taking a look into our support of paid modifications. In the past, these have been banned from being posted anywhere on the forum. Paid authors create some great things, so we’d like to embrace them more going forward. Our current solution is allowing paid modifications in the Requests/Services/Jobs forum, which you can find below.

We’re also considering the possibility of adding thread prefixes to the Requests/Services/Jobs forum in an effort to easily distinguish the types of services available. If you have any suggestions regarding these categories, we’re all ears!

<a href="https://community.mybb.com/forum-190.html" class="button">{% include icon.html icon='comments' %} Visit Forum</a>

## MyBB Software Development Path

After a lot of discussion internally, on the forum and in Discord, we’ve decided on the path that the MyBB software will be following leading up to MyBB 2. While we can all agree that MyBB needs to be more modern, rewriting it entirely from scratch is an enormous task and is taking much longer than we anticipated. Judging from the input from users, as well as discussion among staff, our best option moving forward will be to further bridge the 1.x series toward MyBB 2, while updating it to be more usable and modern.

<a href="{{ site.baseurl }}/assets/images/2017/10/17-screen.png" class="blog-post__image-link"><img src="{{ site.baseurl }}/assets/images/17-screen.png" alt="MyBB Poll results" class="blog-post__image-link__image" /></a>

We have not decided on any specifics, but have discussed some of the following options:

- Use Twig
- Use Sass
- New, responsive theme
- Improved user experience, meaning changes like alerts or conversations

All that we know for now is that the MyBB 1.x line needs to be improved, and we need your help on deciding what exactly will be changing. If you’d like to join in on the discussion, head over to the forum thread we’ve been using to discuss the software.

<a href="https://community.mybb.com/thread-213361.html" class="button">{% include icon.html icon='comments' %} Visit Thread</a>

## Moving Forward

Overall we think these changes will help bring MyBB into the modern age, and make things a lot more fun to take part in. We love reading what you, the users of MyBB have to say and take it *all* into consideration. If you’d like to have a discussion with us, please hop on Discord and let us know about it!

<a href="https://discordapp.com/invite/rX8VpBr" class="button" style="background-color: #7289DA; border-color: #7289DA">{% include icon.html icon='discord' %} Join Discord</a>
