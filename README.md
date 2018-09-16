> This package has been moved to the [pnpm](https://github.com/pnpm/pnpm) multi-package repository.

# @pnpm/modules-yaml

> Reads/writes \`node_modules/.modules.yaml\`

<!--@shields('npm', 'travis')-->
[![npm version](https://img.shields.io/npm/v/@pnpm/modules-yaml.svg)](https://www.npmjs.com/package/@pnpm/modules-yaml) [![Build Status](https://img.shields.io/travis/pnpm/modules-yaml/master.svg)](https://travis-ci.org/pnpm/modules-yaml)
<!--/@-->

## Installation

```sh
npm i -S @pnpm/modules-yaml
```

## Usage

```ts
import {write, read} from '@pnpm/modules-yaml'

await write('node_modules', {
  hoistedAliases: {}
  independentLeaves: false,
  layoutVersion: 1,
  packageManager: 'pnpm@1.0.0',
  pendingBuilds: [],
  shamefullyFlatten: false,
  skipped: [],
  store: '/home/user/.pnpm-store',
})

const modulesYaml = await read(`node_modules`)
```

## API

### `read(pathToDir): Promise<ModulesObject>`

Reads `.modules.yaml` from the specified directory.

### `write(pathToDir, ModulesObject): Promise<void>`

Writes a `.modules.yaml` file to the specified directory.

## License

[MIT](./LICENSE) © [Zoltan Kochan](https://www.kochan.io/)
