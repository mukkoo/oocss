# OOCSS

Object Oriented CSS (for SASS) guideline.

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
### Tasks
### Config
