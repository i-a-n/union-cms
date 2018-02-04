# Union CMS: A Lektor Fork for Server-Side Editing

The purpose of this fork is to better support remote/server-side editing of the Lektor static CMS system. Lektor is great, but only has support for editing of Lektor sites on your local client (sites are then remotely synced to the production server, once built locally). In order to facilitate remote editing by multiple authors, Union CMS hopes to provide:

- Support for running the Lektor admin on a remote server
- A method for multiple authors to log in
- A "local" publish option, which will simply `cp` the build to the proper folder locally
- Easy instructions for how to set up both the editor and the published site on the same server

In addition, Union CMS will also hope to one day have:

- Material Design theme on the editor itself
- A way to customize the editor (colors and logos)
- A better way to attach images to individual pages
- JSON responses automatically generated for certain meta data
- Some way for multiple logins to be managed through the interface

As a result:

- Windows and Mac support may lapse, and eventually be removed
- The desktop app will no longer be supported

## The original Lektor README follows:

Lektor is a static website generator.  It builds out an entire project
from static files into many individual HTML pages and has a built-in
admin UI and minimal desktop app.

<img src="https://raw.githubusercontent.com/lektor/lektor-assets/master/screenshots/admin.png" width="100%">

To see how it works look at the ``example`` folder which contains a
very basic project to get started.

For a more complete website look at [lektor/lektor-website](https://github.com/lektor/lektor-website)
which contains the sourcecode for the official lektor website.

## How do I use this?

For installation instructions head to the official documentation:

* [Installation](https://www.getlektor.com/docs/installation/)
* [Quickstart](https://www.getlektor.com/docs/quickstart/)

## Want to develop on Lektor?

This gets you started:

```
$ git clone https://github.com/lektor/lektor
$ cd lektor
$ virtualenv venv
$ . venv/bin/activate
$ pip install --editable .
$ make build-js
$ make install-git-hooks
$ export LEKTOR_DEV=1
$ lektor quickstart --path example-project
$ lektor --project example-project server
```

If you want to run the test suite instead:

```
$ virtualenv venv
$ . venv/bin/activate
$ pip install --editable ".[test]"
$ make test
```
