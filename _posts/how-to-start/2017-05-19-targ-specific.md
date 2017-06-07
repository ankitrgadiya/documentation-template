---
layout: default
group: how-to-start
permalink: /how-to-start/targ/
---

This template is based on Jekyll and hence you have to have following packages
installed on your system to test changes:
* [Ruby](https://www.ruby-lang.org/en/)
* [Jekyll Gem](https://jekyllrb.com/)


An official documentation of `Jekyll` installation can be found
[here](https://jekyllrb.com/docs/installation/).

#### File Structure:

```
.
├── _data
│   ├── group1.yml
│   ├── group2.yml
│   ├── revision.yml
│   └── navigation.yml
│
├── _layouts
│   ├── default.html
│   └── error.html
│
├── _posts
│   ├── section 1
│   │   └── articles
│   ├── section 2
│   │   └── articles
│   └── section 3
│       └── articles
│
├── assets
│   ├── css
│   │   └── documentation.css
│   └── images
│       └── logo.png
│
├── license.md
├── LICENSE
├── index.md
├── _config.yml
├── 404.md
├── README.md
├── TODO.md
└── .gitignore

```


To start first edit the following in the `_config.yml`:
* `title`
* `baseurl`
* `author`
* `author-link`
* `repo`

##### Note: For Targ documentation keep baseurl variable same as title, with all lowercase and replace space with hypen.
e.g.:
```
title: Documentation Template
baseurl: documentation-template
```

Once, this is done now you can run `Jekyll` server and preview changes live.
We've changed \_config.yml file prior because Jekyll checks it only once before
generating site.
```bash
$ jekyll serve
```
This command will start a server on Localhost which will listen on port 4000 by
default. To test the live version, just open up a Web browser and type
`localhost:4000` in the URL bar.

A website similar to this one will pop up.

That's it.
