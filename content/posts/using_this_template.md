---
title: "Using this template"
date: 2020-04-06T20:14:16-04:00
draft: false
---

# Setting up a new site

- Edit the config.yml for site name.
- Edit `content/_index.md` to update the index page content
<!--more-->
- Edit this file, `content/posts/using_this_template.md`)
- Create new markdown files under `content/posts` for new posts.

# Highlight code

One of the nice things about this setup is good support code syntax highlighting.

Here is an example of the syntax used:

{{< highlight go "hl_lines=4 8" >}}
	renderer := html.NewRenderer(opts)
	output := markdown.ToHTML([]byte(mdFile), nil, renderer)

	oh, err := os.Create("test.html")
	if err != nil {
		panic(err)
	}
	defer oh.Close()

	_, err = oh.Write(output)
	if err != nil {
		panic(err)
	}
{{< / highlight >}}