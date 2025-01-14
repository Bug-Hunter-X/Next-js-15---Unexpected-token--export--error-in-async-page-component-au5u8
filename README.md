# Next.js 15 - Unexpected Token 'export' Error

This repository demonstrates a common error encountered in Next.js 15 when using async functions within page components.  The error arises because of how async/await functions are handled in the context of the component rendering cycle.

## The Problem

The `pages/about.js` file attempts to fetch data asynchronously using `fetch` before rendering the component.  This results in an unexpected token 'export' error.

## Solution

The provided solution uses `getStaticProps` or `getServerSideProps` to fetch data at build time or request time respectively. This resolves the error, ensures proper data fetching, and eliminates the unexpected token error.