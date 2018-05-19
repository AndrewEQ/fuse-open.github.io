---
layout: home
title: Fuse
---

![Fuse Studio](assets/images/header-bg.png)

Welcome to the new home for the [Fuse](https://fusetools.com) Open Source
project.

## What is Fuse?

Fuse is a cross-platform mobile app development tool suite, supporting building
Android and iOS applications. 

With Fuse you can build native mobile user interfaces using the easy to learn UX Markup language, and use JavaScript to add business logic.

## How do I get started?

Well, Fuse is available either as an
[installer from the downloads-page](downloads) for end-user, or
[as source code](source-code) for those who wants to
tinker with the internals.

### Using the installer

The installers are pretty straight-forward; download the right installers
for your operating system (currently supported: Windows and macOS), install
it, and open Fuse.


## How do I join the Fuse community?

You can interact with other fusers on [Slack](https://fusecommunity.slack.com/) or in the [Forums](http://forums.fusetools.com). 

For technical questions, please prefer to use the [community forums](http://forums.fusetools.com). Include as much information as you can about your problem, as well as code to reproduce your issue. This will make it as easy as possible to help, and make your answer searchable for the future. Hundreds of common questions have already been answered. Give the search box a spin before posting :)


<div class="users">
<h2>Fuse Open has been used by top companies from all around the world</h2>
<ul>
{% for user in site.data.users %}
<li><img style="fill: #f0f !important" src="{{ site.baseurl }}/assets/images/users/{{ user.id }}.svg" alt="{{ user.title }}" /></li>
{% endfor %}
</ul>
</div>
