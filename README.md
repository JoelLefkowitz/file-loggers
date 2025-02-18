# File logger

Run tasks over a group of files with progress logs and spinner

![Review](https://img.shields.io/github/actions/workflow/status/JoelLefkowitz/file-loggers/review.yaml)
![Version](https://img.shields.io/npm/v/file-loggers)
![Downloads](https://img.shields.io/npm/dw/file-loggers)
![Size](https://img.shields.io/bundlephobia/min/file-loggers)
![Quality](https://img.shields.io/codacy/grade/b37777bbeb5d417188ae9aee3c9a7c36)
![Coverage](https://img.shields.io/codacy/coverage/b37777bbeb5d417188ae9aee3c9a7c36)

## Motivation

It's a common requirement to run asynchronous tasks over group of files:

![Example](docs/images/example.gif)

This package allows you to simply provide a glob pattern for the files and a callback for each file:

```ts
import { logger } from "file-loggers";

logger(
  "src/**/*.ts",
  async () => {
    await sleep(1000);
    return Math.random() > 0.5 ? "Passing checks ✓" : "Failing checks ✕";
  },
  {
    trail: true,
    count: true,
    timer: true,
  },
);
```

## Installing

```bash
npm install file-loggers
```

## Documentation

Documentation and more detailed examples are hosted on [Github Pages](https://joellefkowitz.github.io/file-loggers).

## Usage

In the example above all the options are enabled:

- `trail` - Show the output from the previous files.
- `count` - Show the index of the current file.
- `timer` - Show the time spent on each file.

They can be independently set to false.

## Tooling

### Dependencies

To install dependencies:

```bash
yarn install
```

### Tests

To run tests:

```bash
yarn test
```

### Documentation

To generate the documentation locally:

```bash
yarn docs
```

### Linters

To run linters:

```bash
yarn lint
```

### Formatters

To run formatters:

```bash
yarn format
```

## Contributing

Please read this repository's [Code of Conduct](CODE_OF_CONDUCT.md) which outlines our collaboration standards and the [Changelog](CHANGELOG.md) for details on breaking changes that have been made.

This repository adheres to semantic versioning standards. For more information on semantic versioning visit [SemVer](https://semver.org).

Bump2version is used to version and tag changes. For example:

```bash
bump2version patch
```

### Contributors

- [Joel Lefkowitz](https://github.com/joellefkowitz) - Initial work

## Remarks

Lots of love to the open source community!

<div align='center'>
    <img width=200 height=200 src='https://media.giphy.com/media/osAcIGTSyeovPq6Xph/giphy.gif' alt='Be kind to your mind' />
    <img width=200 height=200 src='https://media.giphy.com/media/KEAAbQ5clGWJwuJuZB/giphy.gif' alt='Love each other' />
    <img width=200 height=200 src='https://media.giphy.com/media/WRWykrFkxJA6JJuTvc/giphy.gif' alt="It's ok to have a bad day" />
</div>
