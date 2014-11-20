# OOCSS

Object Oriented CSS (for SASS) guideline.

## Skeleton

This is the basic skeleton of yout CSS organization.
Found it in `template/` folder.

```
├── assets
│   ├── fonts
│   └── images
├── models
├── services
├── variables
└── views
    └── layouts

```
### What does they contain?

`assets`: The assets like fonts & images. Idea: Different subfolders for different type or format (ex: in fonts svg, ttf, etc..)
`models`: Each view have 'elements' with common properties. This is our model.
`services`: In this folder there are mixins.
`variables`: This folder contain colors, breakpoints, typography, etc..
`views`: Here the view organizaton of our models.
