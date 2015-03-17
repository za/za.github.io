---
layout: post
title: "Melbourne Django Hack Weekend"
date: 2015-03-18 07:18:20
tags: "python melbourne django melb-django django-dequorum"
---

Wow, it's already March 2015 and I haven't written anything since then here. 

On March 9, it was public holiday at Victoria. So it was a long weekend. I received invitation to join melb-django hack weekend. Since I didn't have any schedule yet, I decided to join and get ready for my first time hack experience.

The hack weekend lasted for two days: on Sunday March 8 and on Monday March 9. Unfortunately I could only joined on Sunday. Actually it will be great if I could join the second day, because on the first day I spent most of my time for setting up the environment.

Since no one had an idea what django project/app to hack, Curtis decided to continue the previous hack project which was [django-dequorum](https://github.com/funkybob/django-dequorum). Curtis explained what is django-dequorum and what features which is undone. django-dequorum is a simple forum django application. Users could post threads and other users could make comments. To make things easier what things need to be done, Curtis put them on the [github issues](https://github.com/funkybob/django-dequorum/issues). And we agreed that we will use git flow to hack this django-dequorum. Everyone will fork and make pull request to contribute to this project. 

Suddenly, it was 12.30 So we decided to have lunch before we hack django-dequorum. We walked to Lenthil, a unique canteen at Abbotsford. They provide vegetarian menu. They didn't charge on how much we ate. They put poster explained how they run this canteen and how much does it cost. We put the money inside a box.

 ![Walking to Lenthil](/images/2015-03-melb-django-dequorum.jpg)

After lunch, Nicole took the initiative to do the look and feel. Nicole drew the layout. 

 ![Drawing layout](https://cloud.githubusercontent.com/assets/3323703/6544386/81bd5b9a-c5a1-11e4-8ffc-4b710d523558.jpg)

I didn't join the layout discussion because I was still struggling with the environment setup. At first I setup my environment with python 2.7.x and later I found that they are using python3. So I re-set up my virtualenv. 

And then I was confused. I didn't want git to track changes on the django project directory but I wanted git to track changes on django-dequorum app. I put a symbolic link, still failed. I finally managed with *folder* symbolic link.

Other problem raised after we forked the github repo. How to keep our forked repo updated with funkybob repo? Since I had this problem before so I already knew the answer. I helped my friends on how to add another git remote repository.

I still didn't make any commits to this open source project, but hopefully I could contribute in the future. It was a nice hack weekend with friendly new friends.
