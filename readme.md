# Cubitt Template

A template project to help easily start developing new Cubitt modules.

[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://raw.githubusercontent.com/uu-cubitt/template/master/LICENSE)
[![Build Status](https://travis-ci.org/uu-cubitt/template.svg?branch=master)](https://travis-ci.org/uu-cubitt/template)
[![Test Coverage](https://codeclimate.com/github/uu-cubitt/template/badges/coverage.svg)](https://codeclimate.com/github/uu-cubitt/template/coverage)

## About

This package provides a basic setup for most TypeScript packages in 
the Cubitt framework.

## Features

* git configuration
* NPM (package) configuration
* travis CI configuration
* codeclimate configuration
* tslint configuraion
* typings configuraion
* typescript configuration

## Usage

Clone this template project and then remove the .git folder.
Then initiate a new git repository:

```bash
git clone git@github.com:uu-cubitt/template.git
cd template
rm -rf .git
git init
```

Change the following files:

* rename ```cubitt-template.ts``` to ```cubitt-new-module.ts```
* update the main and typings fields in ```package.json``` and all links with the new module name
* update ```readme.md``` to include information about the new module

Next, create a new Github repository and enable the repository on Travis.
Then commit and push the changes.

```bash
git add --all
git commit -m "Initial setup"
git add remote git@github.com:uu-cubitt/<new module>.git
git push -u origin master
```

After then push is completed, go to [Codeclimate](https://codeclimate.com/dashboard) and add the new repository.
Then navigate to the repository settings - code coverage - javascript
and copy the ```CODECLIMATE_REPO_TOKEN=8e3...``` to the Travis environment.
Then rerun the build on Travis so the coverage information is send to Codeclimate.
(this bare template does not generate coverage information, due to containing no code or tests)

## For developers

To get started:

```bash
npm run dev
```

To run the unit tests:

```bash
npm run test
```

To generate a test coverage report:

```bash
npm run test-coverage
```

To generate documentation:

```bash
npm run typedoc
```

## License

[MIT](LICENSE)

## Changelog

[Changelog](changelog.md)
