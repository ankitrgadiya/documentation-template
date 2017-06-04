---
layout: default
group: how-to-start
permalink: /how-to-start/targ/
---

This template is based on Jekyll and hence you have to have following packages
installed on your system to test changes:
* Ruby
* Jekyll Gem

An official documentation of `Jekyll` installation can be found
[here](https://jekyllrb.com/docs/installation/).
#### File Structure:

```
.
├── _data
│   ├── group1.yml
│   └── navigation`.yml
|
├── _layouts
│   ├── default.html
│   └── error.html
|
├── _posts
│   ├── section 1
│   |   └── articles
│   ├── section 2
│   |   └── articles
│   └── section 3
│       └── articles
|
├── assets
│   ├── css
│   │   └── documentation.css
│   └── images
│       └── logo.png
|
├── license.md
├── index.md
├── _config.yml
└── 404.md

```

<hr>
To start first edit `author` and `author-link` int the `_config.yml`.

Once, this is done now you can run `Jekyll` server and preview changes live.
```bash
$ jekyll serve
```
This command will start a server on Localhost which will listen on port 4000 by
default. To test the live version, just open up a Web browser and type
`localhost:4000` in the URL bar.

A website similar to this one with little changes will pop up. Now, as you're
going to use this template for personal use, you probably want to remove `Targ`
from the title which you can see in the name of the opened tab.

That's it.
