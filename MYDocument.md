# Docsify

## Table of Contents      

<!--- [Docsify](#docsify)-->
- [Docsify](#docsify)
  - [Table of Contents](#table-of-contents)
  - [Introduction of Docsify](#introduction-of-docsify)
  - [Features of Docsify](#features-of-docsify)
  - [Benefits of Docsify](#benefits-of-docsify)
  - [Step by step by guide to installation and setup](#step-by-step-by-guide-to-installation-and-setup)
  - [Configuration](#configuration)
  - [coverPage](#coverpage)
  - [Themes](#themes)
  - [Markdown](#markdown)
  - [Markdown sytax](#markdown-sytax)
  - [Navigation](#navigation)
  - [Sidebar](#sidebar)
  - [hideSidebar](#hidesidebar)
  - [Configuring and enabling the search functionality in Docsify](#configuring-and-enabling-the-search-functionality-in-docsify)
  - [Full text search](#full-text-search)
  - [Emoji](#emoji)
  - [External Script](#external-script)
  - [Deploy](#deploy)
  - [GitHub Pages](#github-pages)
  - [GitLab Pages](#gitlab-pages)
  - [Firebase Hosting](#firebase-hosting)
  - [VPS](#vps)
  - [Netlify](#netlify)
  - [HTML5 router](#html5-router)
  - [Vercel](#vercel)
  - [AWS Amplify](#aws-amplify)
  - [Docker](#docker)
  - [References-](#references-)
  
## Introduction of Docsify

Docsify is a lightweight documentation generator that helps you turn your documentation into a web application. It is designed to be simple, easy to use, and highly customizable. With Docsify, you can write your documentation in Markdown format and have it rendered as a dynamic website.

## Features of Docsify

- No statically built html files
- Simple and lightweight
- Smart full-text search plugin
- Multiple themes
- Useful plugin API
- Compatible with IE11
- Experimental SSR support (example)
- Support embedded files

## Benefits of Docsify

- all-in-one email tracking.
- one-minute installation
- easy-to-use interface
- 24\7 customer support
- Free plan forever

## Step by step by guide to installation and setup

### Requirement of docsify

    - Distributor ID: Ubuntu
    - Description: Ubuntu 22.04.3 LTS
    - Release: 22.04
    - Codename: shrikant 
    
1. Prerequisites:
Ensure you have Node.js and npm (Node Package Manager) installed. You can download and install them from nodejs.org.

Check node version

```bash
node -v
```
Output

shrikant@shrikant:~$ node -v

v12.22.9

Check npm version

```bash
npm -v
```
Output

shrikant@shrikant:~$ npm -v

8.5.1


3. Install Docsify CLI:
Open your command line interface (CLI) and run the following command to install Docsify globally:

```bash
  npm install -g docsify-cli 
```
Check Docsify version
```bash
sudo docsify -v
```
Output

shrikant@shrikant:~$ sudo docsify -v
[sudo] password for shrikant: 

docsify-cli version:

  4.4.4


3.Create a Documentation Directory:
Decide on a directory for your documentation files. Create a new folder, for example, named docs. Navigate to this folder in the CLI:

```bash
mkdir docs
cd docs
```

1. Initialize Docsify:
  
 Inside the docs directory, run the following command to initialize Docsify:

```bash
docsify init .
```

   This command sets up the basic structure for Docsify, including an index.html file.

1. Edit the Configuration (Optional):

   Open the index.html file in a text editor of your choice. You can customize settings such as the sidebar, theme, and other configurations.

2. Write Documentation:

   Create your documentation using Markdown in the docs directory. The main documentation file is often named README.md.

3. Preview Locally:

   Run the following command to preview your documentation locally:

 ```bash

 docsify serve 
 ```

 Visit <http://localhost:3000>

 in your web browser to view your Docsify documentation.

1. Host on GitHub Pages (Optional):

If you want to host your documentation on GitHub Pages, push your docs directory to a GitHub repository, and then go to the repository's settings to enable GitHub Pages with the source branch set to main or master (whichever is your default branch).

Access Online Documentation:

  After enabling GitHub Pages or deploying your Docsify documentation elsewhere, you can access it online using the provided URL.

## Configuration

All core configuration for docsify is done in the index.html file using the window.$docsify script object

## coverPage

You can set a cover page by setting the coverpage to true and creating a _coverpage.md file in your docsify directory.

- Create a "_coverpage.md" file in your docsify directory.
  
- Add the content of coverpage in Markdown format
  
## Themes

There is a handful of themes available, both official and community-made. Copy Vue and buble website custom theme and @liril-net contribution to the theme of the black style.

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/vue.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/buble.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/dark.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/pure.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/themes/dolphin.css" />
```

!> Compressed files are available in /lib/themes/.

<!-- compressed -->

```html
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/vue.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/buble.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/dark.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/pure.css" />
<link rel="stylesheet" href="//cdn.jsdelivr.net/npm/docsify/lib/themes/dolphin.css" />
```

## Markdown

Markdown is a free markup language with simple formatting syntax. Use it for creating webpages, documents or any text that needs to be transformed into other formats like HTML.

It makes it easier for non-tech writers to produce documentation that can be collaborative and flexible at the same time.

## Markdown sytax

 [Syntax](https://www.markdownguide.org/basic-syntax/)

## Navigation

By default, you won't be able to see the Navbar on your Docsify site:
navbar
No Navar

But don't worry, you can change that. To show the Navbar, you first have to enable it like this:

<!-- index.html -->
```html <script>
      window.$docsify = {
       
        
        loadNavbar: true,     <!-- enable navbar -->
       
      };
    </script>
  </body>
</html>
```

Then create a new _navbar.md file at the root level and paste the following code:

- Getting started

- [Quick start](quickstart.md)

- [Writing more pages](more-pages.md)

- [Custom navbar](custom-navbar.md)

- [Cover page](cover.md)
  
- Configuration
  
- [Configuration](configuration.md)
  
- [Themes](themes.md)
  
- [Using plugins](plugins.md)
  
- [Markdown configuration](markdown.md)

-[Language highlight](language-highlight.md)

Paste the following code in the _navbar.md file

Your Navbar should now look like this:
customizer-navbar
Customize Navbar in Docsify

## Sidebar

In order to have a sidebar, you can create your own '_sidebar.md.'First, you need to set loadSidebar to true.

```html
<!-- index.html -->

<script>
  window.$docsify = {
    loadSidebar: true
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>
```

Create _sidebar.md,In the root of your documentation folder, create a file named_sidebar.md. This file will contain the structure of your sidebar. For example:

```bash
- [Home](README.md)
- [Draft Article](draft-article.md)
- [Guide](guide.md)
- [intro](intro.md)
- [Second](page-second.md)
- [Third](page-third.md)
- [Four](page-four.md)
```

After making these changes, when you run Docsify, you should see a sidebar on the left side of your documentation with the structure specified in the _sidebar.md file.

## hideSidebar

This option will completely hide your sidebar and won't render any content on the side.

```html

window.$docsify = {
  hideSidebar: true,
};
 ```

## Configuring and enabling the search functionality in Docsify

## Full text search

By default, the hyperlink on the current page is recognized and the content is saved in localStorage. You can also specify the path to the files.

```html
<script>
  window.$docsify = {
    search: 'auto', // default
    search: [
      '/',            // => /README.md
      '/guide',       // => /guide.md
      '/get-started', // => /get-started.md
      '/zh-cn/',      // => /zh-cn/README.md
    ],
    // complete configuration parameters
    search: {
      maxAge: 86400000, // Expiration time, the default one day
      paths: [], // or 'auto'
      placeholder: 'Type to search',
      // Localization
      placeholder: {
        '/zh-cn/': '搜索',
        '/': 'Type to search',
      },
      noData: 'No Results!',
      // Localization
      noData: {
        '/zh-cn/': '找不到结果',
        '/': 'No Results',
      },
      // Headline depth, 1 - 6
      depth: 2,
      hideOtherSidebarContent: false, // whether or not to hide other sidebar content
      // To avoid search index collision
      // between multiple websites under the same domain
      namespace: 'website-1',
      // Use different indexes for path prefixes (namespaces).
      // NOTE: Only works in 'auto' mode.
      //
      // When initialiazing an index, we look for the first path from the sidebar.
      // If it matches the prefix from the list, we switch to the corresponding index.
      pathNamespaces: ['/zh-cn', '/ru-ru', '/ru-ru/v1'],
      // You can provide a regexp to match prefixes. In this case,
      // the matching substring will be used to identify the index
      pathNamespaces: /^(\/(zh-cn|ru-ru))?(\/(v1|v2))?/,
    },
  };
</script>

<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>

<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/search.min.js"></script>
```

## Emoji

Renders a larger collection of emoji shorthand codes. Without this plugin, Docsify is able to render only a limited number of emoji shorthand codes.

```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```

## External Script

If the script on the page is an external one (imports a js file via src attribute), you'll need this plugin to make it work.

```html
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/external-script.min.js"></script>
```

## Deploy

Similar to [GitBook](https://www.gitbook.com), you can deploy files to GitHub Pages, GitLab Pages or VPS.

## GitHub Pages

There are three places to populate your docs for your GitHub repository:

- `docs/` folder
- main branch
- gh-pages branch

It is recommended that you save your files to the `./docs` subfolder of the `main` branch of your repository. Then select `main branch /docs folder` as your GitHub Pages source in your repository's settings page.

![GitHub Pages](_images/deploy-github-pages.png)

!> You can also save files in the root directory and select `main branch`.
You'll need to place a `.nojekyll` file in the deploy location (such as `/docs` or the gh-pages branch)

## GitLab Pages

If you are deploying your master branch, create a `.gitlab-ci.yml` with the following script:

?> The `.public` workaround is so `cp` doesn't also copy `public/` to itself in an infinite loop.

```YAML
pages:
  stage: deploy
  script:
  - mkdir .public
  - cp -r * .public
  - mv .public public
  artifacts:
    paths:
    - public
  only:
  - master
```

!> You can replace script with `- cp -r docs/. public`, if `./docs` is your Docsify subfolder.

## Firebase Hosting

!> You'll need to install the Firebase CLI using `npm i -g firebase-tools` after signing into the [Firebase Console](https://console.firebase.google.com) using a Google Account.

Using a terminal, determine and navigate to the directory for your Firebase Project. This could be `~/Projects/Docs`, etc. From there, run `firebase init` and choose `Hosting` from the menu (use **space** to select, **arrow keys** to change options and **enter** to confirm). Follow the setup instructions.

Your `firebase.json` file should look similar to this (I changed the deployment directory from `public` to `site`):

```json
{
  "hosting": {
    "public": "site",
    "ignore": ["firebase.json", "**/.*", "**/node_modules/**"]
  }
}
```

Once finished, build the starting template by running `docsify init ./site` (replacing site with the deployment directory you determined when running `firebase init` - public by default). Add/edit the documentation, then run `firebase deploy` from the root project directory.

## VPS

Use the following nginx config.

```nginx
server {
  listen 80;
  server_name  your.domain.com;

  location / {
    alias /path/to/dir/of/docs/;
    index index.html;
  }
}
```

## Netlify

1.Login to your [Netlify](https://www.netlify.com/) account.

2.In the [dashboard](https://app.netlify.com/) page, click **New site from Git**.
   Choose a repository where you store your docs, leave the **Build Command** area blank, and fill in the Publish directory area with the directory of your `index.html`. For example, it should be docs if you populated it at `docs/index.html`.

## HTML5 router

When using the HTML5 router, you need to set up redirect rules that redirect all requests to your `index.html`. It's pretty simple when you're using Netlify. Just create a file named `_redirects` in the docs directory, add this snippet to the file, and you're all set:

```sh
/*    /index.html   200
```

## Vercel

1. Install [Vercel CLI](https://vercel.com/download), `npm i -g vercel`
2. Change directory to your docsify website, for example `cd docs`
3. Deploy with a single command, `vercel`

## AWS Amplify

1. Set the routerMode in the Docsify project `index.html` to _history_ mode.

```html
<script>
  window.$docsify = {
    loadSidebar: true,
    routerMode: 'history',
  };
</script>
```

   Login to your [AWS Console](https://aws.amazon.com).
 Go to the [AWS Amplify Dashboard](https://aws.amazon.com/amplify).
2. Choose the **Deploy** route to setup your project.
3. When prompted, keep the build settings empty if you're serving your docs within the root directory. If you're serving your docs from a different directory, customise your amplify.yml

```yml
version: 0.1
frontend:
  phases:
    build:
      commands:
        - echo "Nothing to build"
  artifacts:
    baseDirectory: /docs
    files:
      - '**/*'
  cache:
    paths: []
```

6 Add the following Redirect rules in their displayed order. Note that the second record is a PNG image where you can change it with any image format you are using.

| Source address | Target address | Type          |
| -------------- | -------------- | ------------- |
| /<\*>.md       | /<\*>.md       | 200 (Rewrite) |
| /<\*>.png      | /<\*>.png      | 200 (Rewrite) |
| /<\*>          | /index.html    | 200 (Rewrite) |

## Docker

- Create docsify files

  You need prepare the initial files instead of making them inside the container.
  See the [Quickstart](https://docsify.js.org/#/quickstart) section for instructions on how to create these files manually or using [docsify-cli](https://github.com/docsifyjs/docsify-cli).

  ```sh
  index.html
  README.md
  ```

  - Create Dockerfile

  ```Dockerfile
    FROM node:latest
    LABEL description="A demo Dockerfile for build Docsify."
    WORKDIR /docs
    RUN npm install -g docsify-cli@latest
    EXPOSE 3000/tcp
    ENTRYPOINT docsify serve .

  ```

  The current directory structure should be this:

  ```sh
   index.html
   README.md
   Dockerfile
  ```

- Build docker image

  ```sh
  docker build -f Dockerfile -t docsify/demo .
  ```

- Run docker image

  ```sh
  docker run -itp 3000:3000 --name=docsify -v $(pwd):/docs docsify/demo
  ```

## References-
  
- <https://www.freecodecamp.org/news/how-to-write-good-documentation-with-docsify/#basic>
- <https://docsify.js.org/#/>
  
- <https://docs.developer.tech.gov.sg/docs/documentation-portal-publisher-guide/advanced/markdown-features>
  
