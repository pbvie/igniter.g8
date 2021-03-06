# Igniter

![Scala CI](https://github.com/pbvie/igniter.g8/workflows/Scala%20CI/badge.svg?branch=master) [![CircleCI](https://circleci.com/gh/pbvie/igniter.g8.svg?style=svg)](https://circleci.com/gh/pbvie/igniter.g8)

A [Giter8](http://www.foundweekends.org/giter8/) template for kickstarting a new opinionated Scala [playground](#what-is-a-playground-project) project with the following features:

* a tidy `build.sbt` inspired by [sbt-fresh](https://github.com/sbt/sbt-fresh/)
* sensible compiler options
* slim base: almost all (upcoming) features are optional
* formatting with [scalafmt](https://scalameta.org/scalafmt/)
* formatting rules based on Typelevel [Cats](https://github.com/typelevel/cats) with some small adaptions
* clear and colorful logging on the console
* MUnit as test framework
* build using GitHub actions (optional)
* circleci build script (optional)
* cats-core dependency (optional)
* an empty `.gitignore` (read more [here](#why-is-gitignore-empty))

## Usage

```
sbt new pbvie/igniter.g8
```

## Configuration Options

| Property          | Default         | Description                                                      | Example         |
| ----------------- | --------------- | ---------------------------------------------------------------- | --------------- |
| project_name      | awesome-project | The project name used in build.sbt                               | awesome-project |
| organization      | ig.ni.ter       | Organization domain (usually in reverse)                         | io.awesome      |
| organization_name | Igniter         | Organization name                                                | Awesome Org     |
| package           | $organization$  | The base package name (used for code gen)                        | io.awesome      |
| circleci          | true            | Whether a build definition for circleci should be included       | false           |
| gh_actions        | true            | Whether a build definition for GitHub Actions should be included | false           |
| cats              | false           | Adds a dependency on cats-core                                   | true            |

## Roadmap

Have a look at the [project board](https://github.com/pbvie/igniter.g8/projects/2).

## Tip: Run your GitHub Actions locally

You can run your GitHub Actions locally with [act]("https://github.com/nektos/act").

## What is a playground project?

It's what I call a project whose main purpose is to try out or learn something new. As such, it doesn't provide features like

* support for automatic releases
* license management/automatic creation of file headers
* logging config suitable for production

## Why is `.gitignore` empty?

Trying to create and maintain a `.gitignore` file that covers all IDEs, build tools and operating systems out there doesn't seem like the right approach to me. Instead, everybody should create a personal `.gitignore` covering their personal setup and put those rules into their (personal) global `.gitignore`.

You can usually find that global `.gitignore` file at `$HOME/.gitignore`.

What should go into the project-specific `.gitignore`? For example, files that are created by this specific project (like log files) that you don't want to put under version control.

## Template license

To the extent possible under law, the author(s) have dedicated all copyright and related
and neighboring rights to this template to the public domain worldwide.
This template is distributed without any warranty. See <http://creativecommons.org/publicdomain/zero/1.0/>.
