# Jamstack.club?

[Jamstack.club](https://jamstack.club) is a collection of free Jamstack Themes for Hugo, Eleventy, Jekyll, Gatsby and [many other static-sites generators](https://jamstack.club/ssg).  
Filter, sort, preview, and find the best Jamstack Theme for your next project!

[![Screenshot of the homepage of jamstack club](https://raw.githubusercontent.com/RoneoOrg/jamstack.club/main/static/images/cards/overview-second-md.jpg)](https://jamstack.club)

## Contribute

Willing to help? Welcome aboard!

**There are many ways you can contribute**, please read on!  
**We value each contribution** and, if you wish, we can acknowledge you using the [@allcontributors](https://github.com/all-contributors/all-contributors#readme) principles.

### Report a problem

Found an issue? You can [submit a bug report](https://github.com/RoneoOrg/jamstack.club/issues), or [drop us an email](https://jamstack.club/contact/).

We'll get back to you as soon as possible.

### Submit a new theme

There are only two requirements for submitting a theme:

* The source code must be open-source and public
* The demo URL links must point to a demo of the theme and not a personal/business site.

Ready? Let's go!

1. Open [this template file](https://github.com/RoneoOrg/jamstack.club/edit/main/archetypes/theme-template.md) and confirm the creation of a fork.  
(See [the Github documentation](https://docs.github.com/en/repositories/working-with-files/managing-files/editing-files#editing-files-in-another-users-repository) for details, and reach out if you're stuck somewhere!)
2. Edit the file and click on "Propose changes" at the bottom.
3. Submit the Pull Request.
4. You're done!

Yes, the screenshot and the demo page; the Github stars — everything is generated automatically!

## How does it work?

Each theme is described in a Markdown file. (See [this example of a theme specification](https://raw.githubusercontent.com/RoneoOrg/jamstack.club/main/content/theme/hugo-restaurant.md) to get an idea).

The website is built with [Hugo](https://gohugo.io) along with [a few JS scripts](https://github.com/RoneoOrg/jamstack.club/tree/main/scripts) to automate the creation of the Github stats and generate a screenshot.

A [dedicated page](https://jamstack.club/theme/hugo-restaurant/) is created for each theme, as well as [a theme demo website](https://jamstack.club/demo/theme/hugo-restaurant/), at the 'Demo' URL filled out in the Markdown file.

The index is updated, still automatically, and the website is published. It is hosted by [Netlify](https://www.netlify.com/) with a landing at [Jamstack.club](https://jamstack.club).


## Develop Locally

Github stars, image thumbnails and last commit date are generated at build time when this site is deployed to Netlify. Basically the Netlify site runs `npm run deploy`

This site is built on [Hugo](https://gohugo.io/)

Development Server

```
hugo serve
```

Build Site

```
hugo
```

Generate Github stars, image screenshots etc

```
npm install
export GITHUB_TOKEN=XXX
npm run deploy
```

> Generating github data requires a Github Token. You can generate this token in your Github account at settings > developer settings > personal access tokens https://github.com/settings/tokens

## Submitting New Categories
Themes can be categorised with terms from these 4 taxonomies. `ssg`, `cms`, `css` and `archetype`

If you are adding a theme which uses an SSG or CMS which doesnt exist you will need to add it as part of your pull-request.

1. Create a new taxonomy term by creating the markdown file under `content/ssg/` or `content/cms`. For example let's say you wanted to add a new SSG called "Super Duper". Add a file under `content/ssg/super-duper/_index.md` and add the following frontmatter
```
---
title: "Super Duper"
icon: images/icons/super-duper.svg 
official_url: https://super-duper.org
---
```

2. Add the icon. You will need to upload an icon into `static/images/icons`. The icon should in SVG format under 3KB. If it's a PNG please make sure the size is 60x60px and the size is as small as possible (you should be able to keep it under 5KB)
3. Update the Javascript filter logic. Update the file `themes/jamstackthemes/assets/js/filter/filter-groups.js` and add `super-duper` to the ssg array.

## Acknowledgements

See the [About page](https://jamstack.club/about/) for updated acknowledgements and shout-outs!
