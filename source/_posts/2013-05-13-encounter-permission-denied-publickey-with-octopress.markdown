---
layout: post
title: "Encounter Permission denied (publickey) with Octopress"
date: 2013-05-13 01:07
comments: true
categories: [Ocotopress, GitHub, SSH]
---
I got this error message when I tried to regenerate the content and push them to GitHub.

It was working just fine when I first set up and push out the first time about a few hours ago, when I was running

{% codeblock %}
rake setup_github_pages
rake generate
rake deploy
{% endcodeblock %}

I have no idea how it worked the first time, but it apparently looks like I don't have the SSH keys set up correctly.

But my problem was that SSH wasn't using the correct private key (github_rsa) because it was looking for a default name (id_rsa).

You can find a GitHub help page that helps you diagnose the reasons when you see this error:
https://help.github.com/articles/error-permission-denied-publickey

GitHub also has a help page about generating SSH keys pairs and upload the public key to GitHub.
https://help.github.com/articles/generating-ssh-keys
