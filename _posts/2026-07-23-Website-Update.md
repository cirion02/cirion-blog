---
layout: post
title: Website Upside
date: 2026-07-23 00:12:00 +1000
tags:
  - programming
  - meta
---
I've updated a good part of this website. (You probably noticed if your bookmark suddenly went to the new landing page.) This was mostly to add some pages that aren't really blog posts. So far I've made a page to show off some websites my friends maintain, a page for recommending music, and a page for looking for blog posts with specific tags.

In addition, I've made it so the tags at the top of each article are clickable, they now redirect to a page where you can see all articles with said tag. In order to not leave this article too short, I'll be explaining how I programmed that feature.

First of all, this website is made using jekyll, a resource for making blogs, which automates a lot of tedious stuff. (For example, these posts are just markdown files with a small header.) The main blog page is automated from a list of every file in my \_posts folder. This is done using the preprocessor. I'm using mostly defaults, which look something like this[^1]:


{% raw %}

```
{%- for post in posts -%}
	<span>{{post.date}}</span>
	<a href="{{post.url}}">
		{{post.title}}
	</a>
{%- endfor -%}
```

{% endraw %}

You can see in this snippet that you can use some simple programming to automate things. The for loop lets me access all of the posts and their metadata.

Now, annoyingly, this preprocessor cannot be used from within \<script\> tags. What I do instead is create an invisible div at the top of the search page, and shove all of the relevant data from each post inside it. From there I can parse the data using static javascript. Finally, I use said javascript to selectively create elements for each blog post that matches the respective tag. I've written url-parameter based search things before, so after figuring out how to grab the data, this part was pretty easy.

Anyways, if you notice something wrong with the website after this update, feel free to let me know.

[^1]: This code strips various css styles, and also simplifies the exact jekyll code. This websites codebase is public on github if you want to see it in full.