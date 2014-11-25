# OOCSS

Object Oriented CSS (for SASS) guideline.

This is a start point to build a convention about the OOCSS.

This structure is hardly inspired by [BEMO](https://github.com/stefanoverna/bemo) and this [RubyDay 2014 talk](https://www.youtube.com/watch?v=fUJOJY_yVXg&list=PL5ImBN21eKvbQ6kH6WCAqj1QqgusGsiO0&index=6).

## What is OOCSS?

CSS is not an object oriented language.
In 2009 Nicole Sullivan introduced this argument ([see the video](http://www.stubbornella.org/content/2009/03/23/object-oriented-css-video-on-ydn/) ) to developers community.

The goal of Object Oriented CSS is the code reuse for faster and more efficient development and mantain.

OOCSS have two main principles:

* Separate structure and skin
* Separate container and content

## Contribute

This project is currently a draft. If you want to contribute make a fork, a pull request, read the TODO.md or simply open an issue with your questions.

## Skeleton

This is the basic skeleton of yout CSS organization.
Found it in `template/` folder.

```
├── assets
│   ├── fonts
│   └── images
├── config
├── models
├── services
├── tasks
├── variables
└── views
    └── layouts

```
### What does they contain?

`assets`: The assets like fonts & images. Idea: Different subfolders for different type or format (ex: in fonts svg, ttf, etc..)

`config`: Contains the initializers.

`models`: Each view have 'elements' with common properties. This is our model.

`tasks`: Contains external usage hooks. Ex: js interaction.

`services`: In this folder there are mixins.

`variables`: This folder contain colors, breakpoints, typography, etc...

`views`: Here the view organizaton of our model

## Guideline

### Models

Naming:

The file name in lower case.
Point to the object class name: CamelCased and singular.

Model settings:

At the start include mixins and initializer that is ALWAYS an extend-only mixin called %new.

All models have width 100%.

Methods:

The subelements are Model's methods always written like > .title

Scopes:

The Model variants are scopes setted by data-scope attribute.

You can see `models/post_content.sass` example.

### Services

Here, simply, the mixins.

### Variables

Here the variables. Surely colors, typography and media queries.

### Views

The views describes the view organization pairing with html views. Here the models (and only the models) have a dimension if needed.

### Assets

Here only the assets files. Never put here sass (or css) files.

### Tasks

Here we can put the 'external' interactions like JS libraries.

Naming:

Every JS library must access to DOM elements pointing to [data-js-interactionname] attribute. Is the same for css rules.

The filename must descrive the interaction.

### Config

It contains the global configurations like the initializer.
