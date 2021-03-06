# Bookiza

Beautiful responsive books. On web.

Bookiza is a book *baking tool* for web. It is a lightweight JavaScript (node LTS+) framework with a browser shim that lets you publish books, magazines or comics online.

<!-- [![Travis](https://img.shields.io/travis/bookiza/bookiza.svg?maxAge=2592000)](https://travis-ci.org/bookiza/bookiza) -->
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](https://commitizen.github.io/cz-cli/)
[![npm](https://img.shields.io/npm/dt/bookiza.svg?maxAge=2592000)](https://www.npmjs.com/package/bookiza)
![alt tag](https://raw.githubusercontent.com/bookiza/bookiza/master/assets/images/bookiza.png)


# Advantage
Bookiza cuts your book writing & publishing time down by half. By _half_, no less! Porting some of the best design and development techniques from the world of rapid app development, Bookiza will let you develop your story (novel, comics, magazine or textbook) into a timeless product, an eternal journey for readers to share an enjoy… no wait, an 'offline-first' + 'iPad-first' codex book app called [Superbook](https://bubblin.io/docs/format).

Now you can get your developer & designer friends to collaborate on your book for a proper layout and [referential accessibility](https://bubblin.io/blog/referential-accessibility).

Produce delightful books that work [everywhere](https://bubblin.io/support) and for everyone!

> Visit the [Bookiza Website](https://bookiza.io) for more details.


### Support

Books written using Bookiza are [supported](https://bubblin.io/support) on every major device, tablet and desktop out there. All it needs is a modern browser and an Internet connection to load the first time.

Here are some [demo books](https://bubblin.io/) with varying implementations of layout, line-tracking and responsive effects.

Despite ubiquity our effort with superbooks points mostly to yielding best reading experiences on tablets i.e. iPads(iOS 7+), Kindle 3 (Silk) and Android 5.0+ phablets. Because, well, even though it's great to support desktops, smartphones, TVs and whatnot, the most ideal situation and surface for reading books is the tablet.

### Documentation

Full documentation is available [here](https://bubblin.io/bookiza/docs/) and [here](https://bubblin.io/cover/official-handbook-by-marvin-danig) and [here](https://bubblin.io/cover/bookiza-framework-by-marvin-danig).

A quick primer on how Superbooks work is [here](https://bubblin.io/docs/concept).


### What you'll need

node > 8.1.3, git-scm, an `api_key` from `https://bubblin.io` and a unixy-style shell environment.

### Setup

```bash
$ npm install -g bookiza
```

> You'll need to install bookiza and shelljs as global.

Check installation with:

```bash
$ bookiza --version
```

> `bookiza` is shortened to alphabet `b` on your terminal as CLI invoker. This is useful when you're creating a relatively longer body of text and it becomes increasingly painful to type full form commands into the abyss.


Next, register Bookiza client with:

```bash
$ bookiza register or $ b z
```

Provide your Bubblin credentials to connect to its sweet POST API. You're all set!

To check:

```bash
$ bookiza whoami or $ b w
```


### Getting started
To bootstrap new project, run:

```bash
$ bookiza new my-awesome-new-book --leafs 40 --template novella        # Creates a project with 40 fresh leafs (80 pages) inside the `manuscript/` folder and applies a responsive `novella` template on it.
```

`cd` into the project and:

```bash
$ bookiza server                  # Opens https://localhost:4567 on your browser!
```

Open the project on your favorite text editor (VSC Sublime Atom or any other) and write away! Once you're ready (or even if you're not) hit:

```bash
$ bookiza publish
```

Your book will be *POST'ed / PATCH'ed* over Bubblin instantly, in real time. Keep updating with reader feedback!


To see full CLI documentation with:

```bash
$ bookiza --help
```

That's it.

### Templates

Bookiza comes along with several FREE, responsive and scalable [templates](https://github.com/bookiza/templates) so that you don’t have to do the layouts yourself.

Feel free to use templates to kickstart your book/magazine in a best possible way and ensure that your work is responsive and [scalable](https://bubblin.io/support) on as many devices as possible.

> We’re accepting new templates for all kinds of longform. Feel free to [fork](https://github.com/bookiza/templates#fork-destination-box) and submit pull requests per following [rules](https://github.com/bookiza/templates#rules) for any kind of book that you may have worked on.


### Configuration

Bookiza and Bubblin default to only the building blocks of web i.e. HTML, CSS & JavaScript. Infact Bubblin accepts only clean and compiled HTML, CSS & JS to render books.

> No preprocessor jugglery is allowed on live books that're meant for the readers!

Bookiza lets you compose your manuscript with any preprocessor or engine you like. There are two ways to configure Bookiza so as to cater to your most general writing needs and at times, needs that are specific to a particular book.


#### `.bookizarc`

When you register bookiza (`$ bookiza register` or `$ b z` ) it will automatically set up the following global runcom (.rc) file at the root. Bookiza will pick up the mode for its generators from this `arc` file.

```
# $ vi .bookizarc

{
  "token": "",
  "username": "",
  "email": "",

  "mode": {
    "HTML": "html",   # markdown, haml, pug etc.
    "CSS": "css",
    "JS": "js",
    "HEAD": "html"
  },

  "urls": {
    "registrationURL": "https://bubblin.io/api/register",
    "baseURL": "https://bubblin.io/api/books/"
  }
}

```

As you can see, configuring bookiza is as simple as setting the `mode` to use preprocessors of your liking. See full list of templating engines & preprocessors that are currently available.

#### `.bookrc`

Similarly, editing mode can also be set on per book basis with the following `rc` configuration inside the root of your project:

```
# $ vi .bookrc

{
  "mode": {
    "HTML": "html",
    "CSS": "css",
    "JS": "js",
    "HEAD": "html"
  }
}

```
In case of conflict of modes between `.bookrc` and `.bookizarc` the book_level configuration i.e. `.bookrc` shall prevail.

### What is Bookiza?

Bookiza is an open source book writing framework that makes your life easy. Be up and running with a manuscript in seconds and publish some of the best most crazy beautiful books that ever existed.

Books baked with Bookiza use building-blocks of web i.e. HTML, CSS and JavaScript (Yeah, we got JS inside e-books!) so now you can spice up your story with underlying code, dynamic illustrations, data visualizations, interactive graphs, visual explanations and what not.

Get the whole web inside your book!

Check out our [demo book](https://bubblin.io/cover/the-solar-system-by-marvin-danig) on your iPad, for example.


### Why a framework & not wordprocessor?
We wanted to be able to write any kind of book — comics, scientific journals, magazines, novels, schoolbooks, textbooks - using the awesomeness of web.

Wordprocessors trump the flexibility that is required for books, comics & magazines that artists all over the world can create. That's not surprising because wordprocessors originally were meant for enterprise documentation (bureaucracy?) only. For things like purchase orders, contracts or legalese which has nothing to do with nice and creative books.

We also wanted books to feel native on the new web -- not like websites that pretend to be books. Be one that handles long form correctly and scales across all the devices and desktops out there, *ala* - responsive, adaptive and scalable (with or without touch capability).

:metal::point_right: A framework with a powerful CL interface also ensures that we can use our existing developer toolchain to mint and print books.


#### What it is not.

:book: Bookiza is not yet another javascript framework (thankfully) for mobile or app development. It doesn't prescribed a pattern or emphasizes MVC or anything like that. Bookiza is also not a blogging solution. If you wish to write short-form essays or blogposts of upto 3-4 pages (or so) we recommend you to go for a blog instead.

At the moment bookiza will bake manuscripts that are at least 4 pages long. Read more about Superbooks on [Bubblin](https://bubblin.io).


### Obsession

Bookiza is *obsessive* about live book editions and quick manuscript turnarounds. Using instant edit2publish state of web to the maximum. Our goal is to optimize books on the web, make it friendlier for people to read, write and connect. Provide a flexibility that book writers haven't had for the last twenty years. A framework that decidely leaves behind the old-school idea of downloading-a-lifeless-artifact called ebook that is nothing but a dull file sponsored by an even older lobby group that wants physical books to thrive and remain on top!.

We want to focus on a future where web and books are unified, in a single resource that is both accessible and available everywhere.


#### Features

* [x] Responsive container by default
* [x] Cover on all major devices and browsers
* [x] Support beautiful typography with @font-faces
* [x] Allow CDN resources for quick load
* [x] Open once, offline forever without needing to download any artifact
* [x] Modular pages that follow web standards
* [x] Visual explanations with in-page JavaScript
* [x] Full-bleed imagery for fashion/lifestyle journals
* [x] Support for WebGL, CSS3 or other HTML5 experiments.
* [x] Searchable & indexable content
* [x] Simplicity of `git`
* [x] Push2Deploy with real-time editions


## The library
Books created via Bookiza can be published directly to [bubblin](https://bubblin.io) - our substrate marketplace for books or you can host the book on your own website too!

Find a selection of *exclusive* and [handpicked books](https://bubblin.io/books) by our community of writers.

## The community

* Follow [@bookiza on Twitter](https://twitter.com/bookiza)
* Have a feature request or find a bug? [Submit an issue](https://github.com/bookiza/bookiza/issues)
* Have a question that's not a feature request or bug report? [Ask on Bookiza Bubblin forum](https://bubblin.uservoice.com/forums/228504-general)
* Read the [Bubblin Blog](https://medium.com/)


## Authors

Created & maintained by [Marvin Danig](https://twitter.com/marvindanig).

Pull requests, [issues](https://github.com/bookiza/bookiza/issues), contribution and [donations](https://bubblin.io/donations/new) are very welcome. Feedback is welcome from both developers & designers!

See the list of [contributors](https://github.com/bookiza/bookiza/graphs/contributors).

## Further development

Our motto: "Books should be a first class citizen of the web" -- let web & books be together, like a single unified resource -- both accessible and *open*!

We're also working on a draft proposal for [spine_url](https://bubblin.github.io/) to bring native support of books on the web -- like single page apps.

### Dependencies

async, superagent, progress, co-prompt, co, path, fs, chalk, commander, string, dateformat, shelljs, os-homedir


### Bookiza Commit Conventions

* [x] PR branches must work everywhere: i.e. should have been tested on all browsers on OSX, Windows & Linux.
* [x] Commit messages must explain whys & whats. Please lint your JS before submitting your features.
* [x] Provide system related information of the dev machine(OS/Browser/Screen).

### Up next

* Introduce preprocessors inside page generators
* TODO: Consider introducing cover attributes within ambit of JSON. Or not.

### LICENSE

TBD. *UNLICENSED*
