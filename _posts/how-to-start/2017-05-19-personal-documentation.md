---
layout: default
group: how-to-start
permalink: /how-to-start/personal/
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
* `repo` [Optional]

Let me explain them one by one.

So, `title` variable is used in title tag,
header. It basically is used to name the site title.

`author` and `author-link` are pretty self explanatory, they are mostly used in
combination to name the author and point to the link.

`repo` variable is optional. It basically is the name of the repository, which
by default is set to be under [Targ-Project](https://github.com/targ-project)
organization. This link can be found in the footer of any page of this template.
If you don't want it, then comment this line out. Otherwise, if you want this
but want to point towards repository not under
[Targ-Project](https://github.com/targ-project) then do the following:
* Open `./layouts/default.html`.
* Look for a tag in the footer section which would look something like this
  ```
  <div class="col-sm-4 col-md-4 text-center">
    <a href="https://github.com/targ-project/{{site.repo}}">
      Contribute
    </a>
  </div>
  ```
* Change the link to whatever you want. You can even remove the repo variable
  and directly point towards the page you want.
* Do the same in `./layouts/error.html` file.

`baseurl` needs some sort of explaination. It basically is a trick to manage
relative URL when the site is not under root domain. For example, this site is
at `https://targ.ga/documentation-template/` and not at `https://targ.ga/`. So,
we cannot use relative URL directly or else they will get append to the root
domain, i.e., `https://targ.ga/`. So, to overcome this problem, `baseurl`
variable is defined in the `_config.yml` file, or in other words, it is defined
globally. Then we use `{{site.baseurl}}` before all the relative URL and it
works.

A question may arise that why not use absolute URL, but there are a lot of
problems with that, the biggest of all is that you won't be able to test changes
locally, even though it will work on production environment.

So, as you can conclude from the above discussion that, baseurl only makes sense
when the website is not on the root domain. But if you are trying to use this
template for the root domain then assign `/` value to the `baseurl` variable.


Once, this is done now you can run `Jekyll` server and preview changes live.
We've changed \_config.yml file prior because Jekyll checks it only once before
generating site.
```bash
$ jekyll serve
```
This command will start a server on Localhost which will listen on port 4000 by
default. To test the live version, just open up a Web browser and type
`localhost:4000` in the URL bar.

A website similar to this one with little changes will pop up.

To change _Hosted by Github Pages_ from the footer, do the following:
* Open `./layouts/default.html`.
* Look for a tag in the footer section which would look something like this
  ```
  <div class="col-sm-4 col-md-4 text-center">
    Hosted by <a href="https://pages.github.com" >Github Pages</a>
  </div>
  ```
* Change the text and link to whatever you want. You can even remove the code  
  altogether.
* Do the same in `./layouts/error.html` file.

To change the logo just place a `logo.png` file overwriting the previous one in
`./assets/images` directory.

One of the things you probably have not noticed is that this template comes with
custom 404 error page as well. The motivation for this is that whenever user
type some typo in the link, and the server will return error code 404, then we
can redirect them correctly back to the site. To test this page just type some
random words after the current url, and Jekyll server is inteligent enough to
show up 404 page.
But if you're using it for Personal use then you probably want to change the
horizontal list of links. For this do the following:
* Open `./layouts/error.html`.
* Look for this section in main tag.
  ```
  <li>
    <a href="/">Targ</a>
  </li>
  <li>
    <a href="{{site.baseurl}}">{{site.title}}</a>
  </li>
  <li>
    <a href="/about">About</a>
  </li>
  ```
* Change the `li` or list items according to your needs.


That's it.
