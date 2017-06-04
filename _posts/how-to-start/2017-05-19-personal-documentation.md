---
layout: default
group: how-to-start
permalink: /how-to-start/personal/
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
To start first edit the `_config.yml`. This file defines following global
variables:
* Title of Documentation
* Author
* Author-Link
* Baseurl

Other things are pretty clear by there names, but `baseurl` needs some sort of
explaination. It basically is a trick to manage relative URL when the site is
not under root domain. For example, this page is at
`https://targ.ga/documentation-template/how-to-start/personal/` and not at
`https://targ.ga/`. So, we cannot use relative URL directly or else they will
get append to the root domain, i.e., `https://targ.ga/`. So, to overcome this
problem, `baseurl` variable is defined in the `_config.yml` file, or in other
words, it is defined globally. Then we use `{{site.baseurl}}` before all the
relative URL and it works.

A question may arise that why not use absolute URL, but there are a lot of
problems with that, the biggest of all is that you won't be able to test changes
locally, even though it will work on production environment.

So, as you can conclude from the above discussion that, baseurl only makes sense
when the website is not on the root domain. So, if you are trying to use this
template for the root domain then assign `\` value to the `baseurl` variable.
Otherwise, assign the relative path to the domain where your website is as the
value for `baseurl` variable. For example, this documentation template lives at
`/documentation-template` from the root domain and hence this is the value which
is assigned by default to the `baseurl`.

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

To achive this:

* Open `./layouts/default.html`.
* Go to line `22`.
* Remove `Targ |` from the line.
* Open `./layouts/error.html`.
* Go to line `6`.
* Remove `Targ |` from the line.

You also wanna remove `Targ` from the footer list. For that:

* Open `./layouts/default.html`.
* Go to line `125`.
* Either remove it or change `Targ` and URL with your own.

Changing the logo is what you have to do next.

* Just place a `logo.png` file overwriting the previous one in `./assets/images`
directory.

That's it.
