[![Netlify Status](https://api.netlify.com/api/v1/badges/eadda60c-6780-4720-869d-ea925937a7e2/deploy-status)](https://app.netlify.com/sites/netlify-template-jekyll/deploys)
[![Automated Release Notes by gren](https://img.shields.io/badge/%F0%9F%A4%96-release%20notes-00B2EE.svg)](https://github.com/mindreeper2420/netlify-template-jekyll/blob/master/CHANGELOG.md)

___
# Jekyll Template for Netlify
This is a template for running a Jekyll site on Netlify

The is built using Jamstack (JavaScript, APIs, and Markup) technologies ([What is Jamstack?](https://jamstack.org/)) Specifically, we use the technologies recommended by [Netlify CMS - Jekyll](https://www.netlifycms.org/docs/jekyll/).

  _This is an ongoing project and I welcome contributions. Feel free to [file an issue](https://github.com/mindreeper2420/netlify-template-jekyll/issues/new) or submit a PR against an existing issue. If you wish to contribute to this project, you should fork the project under your own account, and then raise any changes via pull requests._

___
## Deploy to Netlify
Use this deploy button to get your own copy of the repository.

[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/mindreeper2420/netlify-template-jekyll&stack=cms)

This button will do the following:

- Connect to your GitHub account and create a new repository with the name you specify
- Deploy your copy of the repository and setup continuous deployment
- Send an invite to the email address associated with your Netlify account

Accept the invite, set your password, then navigate to `/admin` on your site to log in.

Now you're all set, and you can start customizing your static site!

___
## General Details and Features
 - Static site generator: [Jekyll](https://jekyllrb.com/)
 - Hosting: [Netlify](https://www.netlify.com/)
 - CMS: [Netlify](https://www.netlifycms.org/)
 - Build workflow: [Gulp](https://gulpjs.com/)
 - UI Framework: [PatternFly](https://patternfly.org/v4)
 - Code highlighting: [Prism.js](https://prismjs.com/)
 - Google Analytics (only in production)
 - Edit page buttons
 - Add page buttons
 - Contact form

___
## Local Development
All processes are controlled through Node/Gulp. Additionally, Jekyll requires that Ruby be installed. If you do not have these installed, you will need to do so before developing for this project. For Ruby, it is recommended to use [RVM](https://rvm.io/).

**Fork and Clone the Repository**
```bash
$ git clone git@github.com:YOUR_USER_NAME/rhddx.git
$ cd rhddx
$ git remote add -f upstream git@github.com:mindreeper2420/netlify-template-jekyll.git
```

**Requirements:**
 - [Node (10+)](https://nodejs.org/en/)
    - _[NVM](https://nodejs.org/en/download/package-manager/#nvm) is recommended_
 - NPM (6+)
 - [Gulp](https://gulpjs.com/)
   - CLI: 2.2.0
   - Local: 4.0.2
 - Ruby (2.6+ - for Jekyll)

### Building the Project

After you have set up your local environment, you can then build the site.
```bash
# Install devDependencies
$ npm install

# Run Gulp Build
$ gulp build
```

After the initial build, you can then run the local development environment by running either `gulp development` or `scripts/./development.sh`.

  - When in development mode, Gulp will watch the project folders for changes. Changes to `.scss` files will rebuild the styles and update the `main.css` file under `_site/assets/`. Changes to any `.html` files will kick of the Jekyll Build process, updating the HTML files under `_site/`

  - To view the site locally, navigate to [localhost:4000](http://localhost:4000/).

### Run Netlify locally (optional)

If you would like to run the build using Netlify's local configuration, you can utilize their built-in CLI and development scripts:
```bash
# Install the Netlify CLI
$ npm install netlify-cli -g

# Start Netlify dev
$ netlify dev
```

  - When running [Netlify locally](https://www.netlify.com/products/dev/), you can stream your dev server to a URL that you can then share. This is best used for local, collaborative development.

### Scripts

```bash
  # Initializes and checks for updates to the git submodule
$ scripts/./submodule.sh

  # Runs the development processes
$ scripts/./development.sh

  # Run Release processes, update Changelog & push to Master
  # replace {{version}} with either major, minor, patch or prerelease
$ scripts/./release.sh {{version}}
```

## Page construction

Each page under is built using Jekyll Frontmatter. Due to the size and complexity of this site, we use multiple variations of the Frontmatter in order to properly sort and render the various examples and documentation. To view how to build a page, check out the [page construction](help/page-construction) file.

## Browser support

This project is supported on the latest version of the following browsers:

 - Chrome
 - Firefox
 - Safari
 - Edge (Chromium)

----
[![ForTheBadge built-with-love](http://ForTheBadge.com/images/badges/built-with-love.svg)](https://GitHub.com/mindreeper2420/)

[![ForTheBadge uses-git](http://ForTheBadge.com/images/badges/uses-git.svg)](https://github.com/topics/git)
[![ForTheBadge uses-html](http://ForTheBadge.com/images/badges/uses-html.svg)](https://github.com/topics/html)
[![ForTheBadge uses-css](http://ForTheBadge.com/images/badges/uses-css.svg)](https://github.com/topics/css)
