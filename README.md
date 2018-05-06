# Starter Web Design

This is my personal starter project for building a new website.
The assumption for this is that good, mantainable css is hard to write and components are one of many solutions.

It contains many opinionated mistakes and I would very much want to know what they are,
if you have an opinion please open a new issue.

## Spec

1. We follow *BEMCSS* conventions with syntax modifications.

    *block__element*--**modifier-class**_modifier

2. We use *namespacing* for making classes more intuitive.

    - Component
    - Layout
    - Utility

### File Structure

The file structure takes idea from [bem's flex](https://en.bem.info/methodology/filestructure/#flex) and adds namespacing (in a naive way).

```
project
├── common.components
│   ├── c-body
│   ├── c-header
│   │   ├── c-header.css
│   │   ├── c-header.html
│   │   ├── c-header.js
│   │   ├── __menu
│   │   │   └── c-header__menu.css
│   │   └── __item
│   │       └── c-header__item.css
│   │
│   ├── c-main
│   ├── c-footer
│   ├── l-grid
│   └── l-container
│
├── custom-name.components --rewrite on top common
│   └── c-header
│       ├── c-header.css
│       └── c-header.html
│
├── templates
│   ├── home
│   │   └── home.html - manually created
│   └── blog
│       └── blog.html - manually created
│
└── generated
    ├── index.html
    ├── common.css
    ├── home
    │   ├── home.html
    │   └── home.css
    │
    ├── blog
    │   ├── blog.html
    │   └── blog.css
    │
    └── package.json
```