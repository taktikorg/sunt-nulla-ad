# UI5 Test runner

[![Node.js CI](https://github.com/taktikorg/sunt-nulla-ad/actions/workflows/node.js.yml/badge.svg)](https://github.com/taktikorg/sunt-nulla-ad/actions/workflows/node.js.yml)
[![Package Quality](https://npm.packagequality.com/shield/@taktikorg/sunt-nulla-ad.svg)](https://packagequality.com/#?package=@taktikorg/sunt-nulla-ad)
[![Known Vulnerabilities](https://snyk.io/test/github/ArnaudBuchholz/@taktikorg/sunt-nulla-ad/badge.svg?targetFile=package.json)](https://snyk.io/test/github/ArnaudBuchholz/@taktikorg/sunt-nulla-ad?targetFile=package.json)
[![@taktikorg/sunt-nulla-ad](https://badge.fury.io/js/@taktikorg/sunt-nulla-ad.svg)](https://www.npmjs.org/package/@taktikorg/sunt-nulla-ad)
[![PackagePhobia](https://img.shields.io/badge/%F0%9F%93%A6package-phobia-lightgrey)](https://packagephobia.com/result?p=@taktikorg/sunt-nulla-ad)
[![MIT License](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FArnaudBuchholz%2F@taktikorg/sunt-nulla-ad.svg?type=shield)](https://app.fossa.com/projects/git%2Bgithub.com%2FArnaudBuchholz%2F@taktikorg/sunt-nulla-ad?ref=badge_shield)
[![Documentation](https://img.shields.io/badge/-%F0%9F%93%9Adocumentation-blueviolet)](https://arnaudbuchholz.github.io/@taktikorg/sunt-nulla-ad/)

A self-sufficient test runner for UI5 applications enabling parallel execution of tests.

> To put it in a nutshell, some UI5 applications have so many tests that when you run them in a browser, it ends up **crashing**. The main reason is **memory consumption** : the browser process goes up to 2 GB and it blows up. JavaScript is based on garbage collecting but it needs time to operate and the stress caused by executing the tests as well as the use of iframes do not let enough bandwidth for the browser to free up the memory.

> This tool is designed and built as a **substitute** of the [UI5 karma runner](https://github.com/SAP/karma-ui5). It executes all the tests in **parallel** thanks to several browser instances *(which also **reduces the total execution time**)*.

## 📚 [Documentation](https://arnaudbuchholz.github.io/@taktikorg/sunt-nulla-ad/)

## 💿 How to install

* Works with [Node.js](https://nodejs.org/en/download/) >= 18
* Local installation
  * `npm install --save-dev @taktikorg/sunt-nulla-ad`
  * Trigger either with `npx @taktikorg/sunt-nulla-ad` or through an npm script invoking `@taktikorg/sunt-nulla-ad`
* Global installation
  * `npm install --global @taktikorg/sunt-nulla-ad`
  * Trigger with `@taktikorg/sunt-nulla-ad`

**NOTE** : additional packages might be needed during the execution (`puppeteer`, `selenium-webdriver`, `nyc`...) . If they are found installed **locally** in the tested project, they are used. Otherwise, they are installed **globally**.

## ⚖️ License
[![FOSSA Status](https://app.fossa.com/api/projects/git%2Bgithub.com%2FArnaudBuchholz%2F@taktikorg/sunt-nulla-ad.svg?type=large)](https://app.fossa.com/projects/git%2Bgithub.com%2FArnaudBuchholz%2F@taktikorg/sunt-nulla-ad?ref=badge_large)

## ⚠️ Breaking changes

| Version | Reason | 
|-|-|
| **5**.0.0 | • Some coverage reports now includes **all** files, leading to a potential decrease of coverage |
| **4**.0.0 | • Drop support of Node.js 16 |
| **3**.0.0 | • Drop support of Node.js 14 |
| **2**.0.0 | • Command line **parameters** as well as configuration file **syntax** have changed |
|| • Dependencies are installed **on demand** |
|| • Browser instantiation command evolved in an **incompatible way** (see [documentation](https://arnaudbuchholz.github.io/@taktikorg/sunt-nulla-ad/browser.html)) |
|| • Output is different (report, traces) |

## ✒ Contributors

* [Marian Zeis](https://github.com/marianfoo): Documentation page revamp [PR #54](https://github.com/taktikorg/sunt-nulla-ad/pull/54)
* [Raj Singh](https://github.com/rajxsingh): Basic HTTP Authentication in Puppeteer [PR #71](https://github.com/taktikorg/sunt-nulla-ad/pull/71)
