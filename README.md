# Docsify

## Introduction of Docsify

Docsify is a lightweight documentation generator that helps you turn your documentation into a web application. It is designed to be simple, easy to use, and highly customizable. With Docsify, you can write your documentation in Markdown format and have it rendered as a dynamic website.

## Features of Docsify

+ No statically built html files
+ Simple and lightweight
+ Smart full-text search plugin
+ Multiple themes
+ Useful plugin API
+ Compatible with IE11
+ Experimental SSR support (example)
+ Support embedded files

## Benefits of Docsify

+ all-in-one email tracking.
+ one-minute installation
+ easy-to-use interface
+ 24\7 customer support
+ Free plan forever

## Step by step by guide to installation and setup

1. Prerequisites:

    Ensure you have Node.js and npm (Node Package Manager) installed. You can download and install them from nodejs.org.

2. Install Docsify CLI:

   Open your command line interface (CLI) and run the following command to install Docsify globally:

~~~ 
    npm install -g docsify-cli 
~~~

3. Create a Documentation Directory:

    Decide on a directory for your documentation files. Create a new folder, for example, named docs. Navigate to this folder in the CLI:

~~~

  mkdir docs
  cd docs

~~~

1. Initialize Docsify:
  
  Inside the docs directory, run the following command to initialize Docsify:

~~~
   docsify init .
~~~

   This command sets up the basic structure for Docsify, including an index.html file.

1. Edit the Configuration (Optional):

   Open the index.html file in a text editor of your choice. You can customize settings such as the sidebar, theme, and other configurations.

2. Write Documentation:

   Create your documentation using Markdown in the docs directory. The main documentation file is often named README.md.

3. Preview Locally:

   Run the following command to preview your documentation locally:

 bash

 docsify serve .

 Visit http://localhost:3000 
 in your web browser to view your Docsify documentation.

8. Host on GitHub Pages (Optional):

   If you want to host your documentation on GitHub Pages, push your docs directory to a GitHub repository, and then go to the repository's settings to enable GitHub Pages with the source branch set to main or master (whichever is your default branch).

1. Access Online Documentation:

  After enabling GitHub Pages or deploying your Docsify documentation elsewhere, you can access it online using the provided URL.



# Configuration

All core configuration for docsify is done in the index.html file using the window.$docsify script object.

## Sidebar

In order to have a sidebar, you can create your own '_sidebar.md.'First, you need to set loadSidebar to true.
```
<!-- index.html -->

<script>
  window.$docsify = {
    loadSidebar: true
  }
</script>
<script src="//cdn.jsdelivr.net/npm/docsify/lib/docsify.min.js"></script>

```

Create _sidebar.md,In the root of your documentation folder, create a file named_sidebar.md. This file will contain the structure of your sidebar. For example:

```

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

```

window.$docsify = {
  hideSidebar: true,
};
```

## coverPage

You can set a cover page by setting the coverpage to true and creating a _coverpage.md file in your docsify directory.

+ Create a "_coverpage.md" file in your docsify directory.
  
+ Add the content of coverpage in Markdown format 
  
Example

## Markdown Usage

## What is Markdown?

Markdown is a free markup language with simple formatting syntax. Use it for creating webpages, documents or any text that needs to be transformed into other formats like HTML.

## Why use Markdown?

It makes it easier for non-tech writers to produce documentation that can be collaborative and flexible at the same time.

## Markdown sytax


 [Syntax](https://www.markdownguide.org/basic-syntax/)

## Navigation and Sidebar

## Configuring and enabling the search functionality in Docsify

## How to integrate Docsify with GitHub

## Available Plugins and Extensions

# List of Plugins

## Full text search

By default, the hyperlink on the current page is recognized and the content is saved in localStorage. You can also specify the path to the files.
```
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
```
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/emoji.min.js"></script>
```

## External Script

If the script on the page is an external one (imports a js file via src attribute), you'll need this plugin to make it work.

```
<script src="//cdn.jsdelivr.net/npm/docsify/lib/plugins/external-script.min.js"></script>
```

# Deploy 
## Vercel
Vercel is a cloud platform that enables developers to deploy and host websites and applications. It is known for its focus on simplicity and speed, making it easy for developers to quickly deploy their projects. Here are some key features and aspects of Vercel

### Installation of vercel
Run the following command to install vercel in your system
```
npm i -g vercel
```
Check the version of your vercel by running the following command:
```
vercel --version
```
Change directory to your docsify website
```
cd Docs
```
login to your vercel account using github.
```
 Log in to Vercel 
● Continue with GitHub 
○ Continue with GitLab 
○ Continue with Bitbucket 
○ Continue with Email 
○ Continue with SAML Single Sign-On 
  ─────────────────────────────────
○ Cancel 
```
```
Please visit the following URL in your web browser:
> Success! GitHub authentication complete for sainiaakash362@gmail.com
? Set up and deploy “~/Docs/Docs”? [Y/n] 
```
Enter Y to deploy your proje
   
 + ### Including instructions on how to integrate and use specific plugins
  
## 
    
## Advanced customization and theme options for modifying the appearance

## References-
  
+ <https://www.freecodecamp.org/news/how-to-write-good-documentation-with-docsify/#basic>
  
+ <https://docs.developer.tech.gov.sg/docs/documentation-portal-publisher-guide/advanced/markdown-features>
  
