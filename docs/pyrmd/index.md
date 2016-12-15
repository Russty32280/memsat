---
layout: page
title: Pyrmd
description: Generate documentation to Markdown
theme: green
---

Pyrmd is a novel, ground-breaking piece of software written by the awesome Michael McCaffrey to automatically generate documentation. It is a Python script which reads all of the source files in a particular directory and parses each one to generate docs in Markdown.

## Usage
`python pyrmd.py {directory} {enable jeykll headers}`

This script can run in any directory by including it as the first parameter. The default is its own directory. When specifying a directory, be sure to include the trailing slash, ie. `memsat/`. To manually enter its own directory, use `./`.

The second parameter, if set, uses Jeykll headers which can be used to generate docs for `memsat.space`. If not set, files will be generated with standard Markdown.

The documentation should be formatted like JavaDocs to be processed correctly.

## Automatic Deployment
Docs can be automatically generated in any repository with a Bash script. It can also be configured on a Continuous Integration server. This file will have to exist in your project folder for it to run.

Run it in a Linux terminal:
`./generate_docs.sh`

As parameters, include your username and password for Git*Lab* and your username and password for Git*Hub*. It will pull `pyrmd` from GitLab, run it, pull the `memsat.space` repository, copy the docs to the website, and upload the new files to the website. This all happens in a single task, without any other user input.

`./generate_docs.sh fleker passwordlab fleker passwordhub`