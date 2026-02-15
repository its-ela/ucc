Chapter 1

* # About React and Next.js
### Building blocks of a web application[](https://nextjs.org/learn/react-foundations/what-is-react-and-nextjs#building-blocks-of-a-web-application)

There are a few things you need to consider when building modern applications. Such as:

- **User Interface** - how users will consume and interact with your application.
- **Routing** - how users navigate between different parts of your application.
- **Data Fetching** - where your data lives and how to get it.
- **Rendering** - when and where you render static or dynamic content.
- **Integrations** - what third-party services you use (for CMS, auth, payments, etc.) and how you connect to them.
- **Infrastructure** - where you deploy, store, and run your application code (serverless, CDN, edge, etc.).
- **Performance** - how to optimize your application for end-users.
- **Scalability** - how your application adapts as your team, data, and traffic grow.
- **Developer Experience** - your team's experience building and maintaining your application.

For each part of your application, you will need to decide whether you will build a solution yourself or use other tools, such as packages, libraries, and frameworks.

### What is React?[](https://nextjs.org/learn/react-foundations/what-is-react-and-nextjs#what-is-react)

[React](https://react.dev/) is a JavaScript **library** for building **interactive user interfaces**.

By user interfaces (UI), we mean the elements that users see and interact with on-screen.

![[Pasted image 20260208182730.png]]

By library, we mean React provides helpful functions (APIs) to build UI, but leaves it up to the developer where to use those functions in their application.

Part of React's success is that it is relatively unopinionated about the other aspects of building applications. This has resulted in a flourishing ecosystem of third-party tools and solutions, including Next.js.

It also means, however, that building a complete React application from the ground up requires some effort. Developers need to spend time configuring tools and reinventing solutions for common application requirements.

## What is Next.js?[](https://nextjs.org/learn/react-foundations/what-is-react-and-nextjs#what-is-nextjs)

Next.js is a React **framework** that gives you building blocks to create web applications.

By framework, we mean Next.js handles the tooling and configuration needed for React, and provides additional structure, features, and optimizations for your application.

but, searching deep down in to the main purpose of Next.js we got that he primary purpose (hasPurpose) of Next.js is to serve as a React framework that provides integrated and optimized solutions for the common challenges of modern web applications (routing, data fetching, hybrid rendering, caching, performance, developer experience — DX), enabling developers to focus on business logic rather than reinventing low-level tools.

![[Pasted image 20260208184704.png]]

Chapter 2

# Rendering User Interfaces (UI)

To understand how React works, we first need a basic understanding of how browsers interpret your code to create (or render) user interfaces (UI).

When a user visits a web page, the server returns an HTML file to the browser that may look like this:

![[Pasted image 20260208200827.png]]

The browser then reads the HTML and constructs the Document Object Model (DOM).

### What is the DOM?[](https://nextjs.org/learn/react-foundations/rendering-ui#what-is-the-dom)

The DOM is an object representation of the HTML elements. It acts as a bridge between your code and the user interface, and has a tree-like structure with parent and child relationships.

![[Pasted image 20260208200926.png]]

ou can use DOM methods and JavaScript, to listen to user events and [manipulate the DOM](https://developer.mozilla.org/docs/Learn/JavaScript/Client-side_web_APIs/Manipulating_documents) by selecting, adding, updating, and deleting specific elements in the user interface. DOM manipulation allows you to not only target specific elements, but also change their style and content.

QUIZ
![[Pasted image 20260208200325.png]]

Chapter 3

Updating UI with JavaScript 

In this chapter, we'll start building out our project by using JavaScript and DOM methods to add an `h1` tag to your project.

Open your code editor and create a new `index.html` file. Inside the HTML file, add the following code:

![[Pasted image 20260210082907.png]]

Then give the `div` a unique `id` so that you can target it later.

![[Pasted image 20260210082940.png]]

