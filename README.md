# Next.js getServerSideProps() Hydration Error with node-fetch

This repository demonstrates a common issue encountered when using `node-fetch` within `getServerSideProps()` in a Next.js application. The problem arises from attempting to use a Node.js module directly in the client-side hydration phase, leading to runtime errors.

## Problem

The `about.js` file uses `node-fetch` to fetch data from an external API within `getServerSideProps()`. This works correctly on the server-side. However, during the client-side hydration, Next.js attempts to execute the same code, resulting in an error because `node-fetch` is not available in the browser environment.

## Solution

The `aboutSolution.js` file offers a solution by using the built-in `fetch` API or a browser-compatible alternative like `isomorphic-unfetch`, which can run seamlessly on both the server and the client-side.  This ensures that the code executes without errors during hydration.

## Setup

1. Clone the repository.
2. Navigate to the project directory.
3. Run `npm install` to install dependencies.
4. Run `npm run dev` to start the development server.

This example showcases the error and its solution, helping developers avoid common pitfalls when integrating external APIs in Next.js applications.