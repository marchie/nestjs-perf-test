# NestJS Performance Test

This is a bare-bones NestJS application that has been setup as follows:

1. Installed the NestJS CLI globally: `npm install -g @nestjs/cli`
1. Created the NestJS application with the CLI: `nest new nestjs-perf-test --skip-git --package-manager npm --language TS --strict`

## Installation

To install, run `npm install`.

## About the tests

The application contains two types of test:

* **Unit tests**, which are executed with the command: `npm run test`; and
* **End-to-end tests**, which are executed with the command: `npm run test:e2e`.

The NPM commands have been modified from the default NestJS config to add these flags:

* **--no-cache**, disabling the Jest cache; and
* **--runInBand**, making the tests run serially, rather than in a worker pool.

These should make the tests more comparable across different systems.

# Results

## Node v18 running on 2019 16-inch MacBook Pro

* **Unit tests:** 
* **End-to-end tests:**

## Node v18 + TypeScript DevContainer running on 2019 16-inch MacBook Pro

* **Unit tests:** `3.362s` `3.25s` `3.519s`
* **End-to-end tests:** `4.035s` `3.961s` `3.997s`