# oclif-hello-world

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->

- [Usage](#usage)
- [Commands](#commands)
<!-- tocstop -->

# Usage

<!-- usage -->

```sh-session
$ npm install -g clitest01
$ clitest01 COMMAND
running command...
$ clitest01 (--version)
clitest01/0.0.0 darwin-x64 node-v16.13.0
$ clitest01 --help [COMMAND]
USAGE
  $ clitest01 COMMAND
...
```

<!-- usagestop -->

# Commands

<!-- commands -->

- [`clitest01 hello PERSON`](#clitest01-hello-person)
- [`clitest01 hello world`](#clitest01-hello-world)
- [`clitest01 help [COMMAND]`](#clitest01-help-command)
- [`clitest01 plugins`](#clitest01-plugins)
- [`clitest01 plugins:install PLUGIN...`](#clitest01-pluginsinstall-plugin)
- [`clitest01 plugins:inspect PLUGIN...`](#clitest01-pluginsinspect-plugin)
- [`clitest01 plugins:install PLUGIN...`](#clitest01-pluginsinstall-plugin-1)
- [`clitest01 plugins:link PLUGIN`](#clitest01-pluginslink-plugin)
- [`clitest01 plugins:uninstall PLUGIN...`](#clitest01-pluginsuninstall-plugin)
- [`clitest01 plugins:uninstall PLUGIN...`](#clitest01-pluginsuninstall-plugin-1)
- [`clitest01 plugins:uninstall PLUGIN...`](#clitest01-pluginsuninstall-plugin-2)
- [`clitest01 plugins update`](#clitest01-plugins-update)

## `clitest01 hello PERSON`

Say hello

```
USAGE
  $ clitest01 hello [PERSON] -f <value>

ARGUMENTS
  PERSON  Person to say hello to

FLAGS
  -f, --from=<value>  (required) Whom is saying hello

DESCRIPTION
  Say hello

EXAMPLES
  $ oex hello friend --from oclif
  hello friend from oclif! (./src/commands/hello/index.ts)
```

_See code: [dist/commands/hello/index.ts](https://github.com/friederbluemle/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `clitest01 hello world`

Say hello world

```
USAGE
  $ clitest01 hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `clitest01 help [COMMAND]`

Display help for clitest01.

```
USAGE
  $ clitest01 help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for clitest01.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `clitest01 plugins`

List installed plugins.

```
USAGE
  $ clitest01 plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ clitest01 plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `clitest01 plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ clitest01 plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ clitest01 plugins add

EXAMPLES
  $ clitest01 plugins:install myplugin

  $ clitest01 plugins:install https://github.com/someuser/someplugin

  $ clitest01 plugins:install someuser/someplugin
```

## `clitest01 plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ clitest01 plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ clitest01 plugins:inspect myplugin
```

## `clitest01 plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ clitest01 plugins:install PLUGIN...

ARGUMENTS
  PLUGIN  Plugin to install.

FLAGS
  -f, --force    Run yarn install with force flag.
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Installs a plugin into the CLI.

  Can be installed from npm or a git url.

  Installation of a user-installed plugin will override a core plugin.

  e.g. If you have a core plugin that has a 'hello' command, installing a user-installed plugin with a 'hello' command
  will override the core plugin implementation. This is useful if a user needs to update core plugin functionality in
  the CLI without the need to patch and update the whole CLI.

ALIASES
  $ clitest01 plugins add

EXAMPLES
  $ clitest01 plugins:install myplugin

  $ clitest01 plugins:install https://github.com/someuser/someplugin

  $ clitest01 plugins:install someuser/someplugin
```

## `clitest01 plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ clitest01 plugins:link PLUGIN

ARGUMENTS
  PATH  [default: .] path to plugin

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Links a plugin into the CLI for development.

  Installation of a linked plugin will override a user-installed or core plugin.

  e.g. If you have a user-installed or core plugin that has a 'hello' command, installing a linked plugin with a 'hello'
  command will override the user-installed or core plugin implementation. This is useful for development work.

EXAMPLES
  $ clitest01 plugins:link myplugin
```

## `clitest01 plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ clitest01 plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ clitest01 plugins unlink
  $ clitest01 plugins remove
```

## `clitest01 plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ clitest01 plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ clitest01 plugins unlink
  $ clitest01 plugins remove
```

## `clitest01 plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ clitest01 plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ clitest01 plugins unlink
  $ clitest01 plugins remove
```

## `clitest01 plugins update`

Update installed plugins.

```
USAGE
  $ clitest01 plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```

<!-- commandsstop -->
