# typescript-starter

[![NPM Version][npm-image]][npm-url] [![Build Status][travis-image]][travis-url] [![Coverage][coveralls-image]][coveralls-url]

A starter project for TypeScript libraries

## Usage

This repository is meant to be forked and kept as another git remote so future
changes can be merged in. The developer should replace all instances of
`typescript-starter` with their package name and change the appropriate fields
in the `package.json`.

## Commands

The default is to use simple npm scripts instead of `gulp` or `grunt` because
it is easier to understand for new developers and reduces the devDependencies.
The `npm run` supports the following commands.

- **prebundle** Automatically run before `bundle`. Compiles the TypeScript and
  moves the files in source into the current working directory.
- **bundle** Generates a master dts file for the package from `index.d.ts`.
- **clean** Removes `build`, `coverage`, and artifacts from `bundle`.
- **precompile** Automatically run before `compile`. Runs `clean`.
- **compile** Compiles the TypeScript.
- **coveralls** Sends code coverage information to Coveralls.
- **lint** Runs `tslint` on all of the files.
- **setup** Removes `node_modules` and `typings` and then runs `npm install` and
  `npm run typings`
- **pretest** Automatically run before `test`. Compiles and modifies the
  compiled JavaScript for sourcemap support and coverage.
- **test** Runs mocha with istanbul code coverage. Set `$MOCHA_REPORTER` to
  override which reporter is used in tests.
- **posttest** Automatically run after `test`. Checks the code coverage and will
  fail if the code coverage is not sufficient. Also runs `lint`.
- **typings** Installs the type definitions.
- **update** Merges from origin master and then runs `npm run setup`.

## Contributing

Feel free to fork and submit pull requests for the configuration. For a sanity
check:

```sh
git clone git@github.com:Asana/typescript-starter.git
cd typescript-starter
npm install
npm run typings
npm test
```

[npm-url]: https://www.npmjs.org/package/typescript-starter
[npm-image]: http://img.shields.io/npm/v/typescript-starter.svg?style=flat-square

[travis-url]: http://travis-ci.org/Asana/typescript-starter
[travis-image]: http://img.shields.io/travis/Asana/typescript-starter.svg?style=flat-square

[coveralls-url]: https://coveralls.io/r/Asana/typescript-starter
[coveralls-image]: https://img.shields.io/coveralls/Asana/typescript-starter/master.svg?style=flat-square
