# Docsify

## Table of Contents      

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
    
  - [References-](#references-)
  
## Introduction of Docsify

Docsify is a lightweight documentation generator that helps you turn your documentation into a web application. It is designed to be simple, easy to use, and highly customizable. With Docsify, you can write your documentation in Markdown format and have it rendered as a dynamic website.

## Features of Docsify

- No statically built html files
- Simple and lightweight
- Smart full-text search plugin
- Multiple themes
- Useful plugin API
- Support embedded files

## Benefits of Docsify

- all-in-one email tracking.
- one-minute installation
- easy-to-use interface
- 24\7 customer support
- Free plan forever

## Step by step by guide to installation and setup

### Requirement of docsify

   - Distributor ID:	Ubuntu
   - Description:	Ubuntu 22.04.3 LTS
   - Release:	22.04
   - Codename:	jammy

    
1. Prerequisites:
Ensure you have Node.js and npm (Node Package Manager) installed. You can download and install them from nodejs.org.

Check node version

```bash
node -v
```
Output


v12.22.9

Check npm version

```bash
npm -v
```
Output


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


![image](https://github.com/kshitizShri929/Docsify/assets/100191247/ee9900ba-c61e-4805-b79b-2704c58ca778)




