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

The time taken to complete each operation in seconds:

## Node v18 running on 2019 16-inch MacBook Pro

* **Unit tests:** `1.809` `1.786` `1.800`
* **End-to-end tests:** `2.060` `2.096` `2.042`

## Node v18 running on Windows laptop

* **Unit tests:** `2.925` `2.807` `2.809`
* **End-to-end tests:** `3.247` `3.251` `3.243`

## Node v18 + TypeScript DevContainer running on 2019 16-inch MacBook Pro

* **Unit tests:** `3.362` `3.250` `3.519`
* **End-to-end tests:** `4.035` `3.961` `3.997`

## Node v18 + TypeScript DevContainer running on employer Windows laptop

* **Unit tests:** `110.700` `75.106` `49.609`
* **End-to-end tests:** `78.201` `70.119` `73.495`

## Node v18 + TypeScript DevContainer running on employer Citrix VDI

* **Unit tests:** `117.327` `135.476` `150.032`
* **End-to-end tests:** `148.107` `139.019` `138.574`
