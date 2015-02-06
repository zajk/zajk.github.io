---
layout: post
title: Vagrant - permanent facts for puppet?
categories: []
tags: []
published: True

---
I was testing some configurations and needed "permanent" facts for mcollective.
Vagrant puppet provisioner has support for facts, but only for provision runs.
Facter supports loading external facts from files in facts.d directory in multiple
format, so I mashed up some ruby code to write hashes as json files and moving them
to facts.d directory before puppet provisioner runs.

Check out Vagrant snippet bellow for more info.

![Vagrantfile snippet]({{ site.url }}/images/permanent_facts_snippet.png)
