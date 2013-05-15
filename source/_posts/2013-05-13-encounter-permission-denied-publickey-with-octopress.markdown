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

But my problem was that SSH wasn't using the correct private key <code>github_rsa</code> because it was looking for a default name <code>id_rsa</code>.

You can find a GitHub help page that diagnoses on the <a href="https://help.github.com/articles/error-permission-denied-publickey">Permission denied (publickey)</a> error.

GitHub also has a help page about <a href="https://help.github.com/articles/generating-ssh-keys">generating SSH keys</a> and upload the public key to GitHub.
