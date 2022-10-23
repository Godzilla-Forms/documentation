# Overview

Let's face it, forms are really verbose in any framework. To make matters worse, most form helpers do way too much magic
and
often have a significant performance cost associated with them. Godzilla is a small library that helps you with the 3
most
annoying parts:

1. Getting values in and out of form state.
2. Validation and error messages.
3. Handling form submission.

By colocating all of the above in one place, Godzilla will keep things organized--making testing, refactoring, and
reasoning about your forms a breeze.

What if you can build your forms in a visual way? Godzilla provides a form builder that allows you to build your forms,
and then export them as JSON, so you can then use the JSON to generate your forms in any framework.

No more writing HTML, CSS and JS for your forms. Just build them in the form builder and export them as JSON.
you can take to step further and make it dynamic by saving the form on Godzilla or your one backend and then use the API
to retrieve the form on the fly.

# Installation

Godzilla have two packages, the core and the parser. The core is the core of the library that's contains all the
models and settings and the parser is the depends on the framework that you are using.

You can install the library with NPM or Yarn.

```bash
 npm install @godzilla/core  --save
 -- OR --
 yarn add @godzilla/core

```

For Angular, you can install the parser with NPM or Yarn.

```bash
 npm install @godzilla/parser  --save
 -- OR --
 yarn add @godzilla/parser

```


