# Welcome to Remix + Express + ShadCN Starter Kit
- The easiest way to get started with Remix, Express, and ShadCN UI.

## Introduction and Inspiration

- I needed a Remix and ShadCN UI setup.
- The steps for [installing ShadCN into Remix](https://ui.shadcn.com/docs/installation/remix) were outdated and unclear (e.g failed to work with the latest version of RemixJS), therefore I had to fight hundreds of bugs while trying to figure out how to make the two work together correctly.
- I also wanted to use Express as the server for my Remix app, so as to open up the possibility of using other Express middlewares and plugins.
- After hours of bad configuration, I figured a way out, and so I decided to avail this repo to the community so that anyone interested can benefit from it and have it easier than I did.
- I hope this repo helps you in your Remix + Express + ShadCN journey.
- Feel free to contribute to this repo by making a PR, if you have any improvements or suggestions.
- Also follow me on Twitter [@DaggieBlanqx](https://twitter.com/DaggieBlanqx) and LinkedIn [DaggieBlanqx](https://www.linkedin.com/in/daggieblanqx/).

## Technologies Used

- 📖 [Remix](https://remix.run/docs)
- [Express](https://expressjs.com/)
- [Shadcn](https://ui.shadcn.com/)
- [Express + Remix explanation](https://remix.run/docs/en/main/discussion/introduction#http-handler-and-adapters)

## Getting Started

- There are two ways to get started with this repo:

  1. (Preferred) Use the Remix CLI to create a new Remix app with this template
  2. (Not recommended) Clone the repo and install the dependencies

  ### 1. Use the Remix CLI to create a new Remix app with this template

  - Run the following command to create a new Remix app with this template:

    ```shell
    npx create-remix@latest --template DaggieBlanqx/remixjs-expressjs-shadcn
    ```

  - You will be prompted to enter the name of your project. Enter it then hit the enter key.
  - After the project is created, cd into the project directory and run the following command to start the dev server:
    ```shell
    cd your-project-name
    npm run dev
    ```

  ### 2. Clone the repo and install the dependencies

  - If you choose #2, you can clone the repo and install the dependencies as follows:

    ```shell
    git clone https://github.com/DaggieBlanqx/remixjs-expressjs-shadcn
    ```

  - Then cd into the project directory and install the dependencies

    ```shell
    cd remixjs-expressjs-shadcn
    npm install
    ```

  - Then run the dev server
    ```shell
    npm run dev
    ```

## Adding ShadCN Components

- If you want to install ShadCN components for example a [button](https://ui.shadcn.com/docs/components/button) component, you can do so by running the following command:

  ```shell
  npx shadcn@latest add button
  ```

- Or maybe let us install ShadCN [table](https://ui.shadcn.com/docs/components/table) component for you:

  ```shell
  npx shadcn@latest add table
  ```

## Code Structure

```shell
.
├── README.md
├── build/                  # Generated by `npm run build`
├── node_modules/           # Generated by `npm install`
├── public/                 # Static files
│   ├── favicon.ico
│   ├── logo-dark.png
│   └── logo-light.png
├── app/
│   ├── components/
│   │   └── ui/             # ShadCN components go into this directory
│   │       └── button.jsx
│   ├── entry.client.jsx    # Client entry point
│   ├── entry.server.jsx    # Server entry point
│   ├── lib/                # Utility functions
│   │   └── utils.js        # ShadCN utilities e.g., tailwind-merge
│   ├── root.jsx            # Root component
│   ├── routes/             # Routes directory
│   │   └── index.jsx       # Renamed from _index.jsx for clarity
│   └── styles/             # CSS files directory
│       └── tailwind.css    # Main tailwind CSS file
├── components.json         # ShadCN components manifest
├── jsconfig.json           # JavaScript configuration
├── package-lock.json
├── package.json
├── postcss.config.js       # PostCSS configuration
├── server.js               # Express server
├── tailwind.config.js      # Tailwind configuration
└── vite.config.js          # Vite configuration
```

## Deployment in Production

First, build your app for production:

```shellell
npm run build
```

Then run the app in production mode:

```shellell
npm start
```

Now you'll need to pick a host to deploy it to.

### DIY

If you're familiar with deploying Node applications, the built-in Remix app server is production-ready.

Make sure to deploy the output of `npm run build`

- `build/server`
- `build/client`
