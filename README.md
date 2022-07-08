oclif-hello-world
=================

oclif example Hello World CLI

[![oclif](https://img.shields.io/badge/cli-oclif-brightgreen.svg)](https://oclif.io)
[![Version](https://img.shields.io/npm/v/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![CircleCI](https://circleci.com/gh/oclif/hello-world/tree/main.svg?style=shield)](https://circleci.com/gh/oclif/hello-world/tree/main)
[![Downloads/week](https://img.shields.io/npm/dw/oclif-hello-world.svg)](https://npmjs.org/package/oclif-hello-world)
[![License](https://img.shields.io/npm/l/oclif-hello-world.svg)](https://github.com/oclif/hello-world/blob/main/package.json)

<!-- toc -->
* [Usage](#usage)
* [Commands](#commands)
<!-- tocstop -->
# Usage
<!-- usage -->
```sh-session
$ npm install -g yp-scrape
$ yp-scrape COMMAND
running command...
$ yp-scrape (--version)
yp-scrape/0.0.0 linux-x64 node-v16.15.1
$ yp-scrape --help [COMMAND]
USAGE
  $ yp-scrape COMMAND
...
```
<!-- usagestop -->
# Commands
<!-- commands -->
* [`yp-scrape hello PERSON`](#yp-scrape-hello-person)
* [`yp-scrape hello world`](#yp-scrape-hello-world)
* [`yp-scrape help [COMMAND]`](#yp-scrape-help-command)
* [`yp-scrape plugins`](#yp-scrape-plugins)
* [`yp-scrape plugins:install PLUGIN...`](#yp-scrape-pluginsinstall-plugin)
* [`yp-scrape plugins:inspect PLUGIN...`](#yp-scrape-pluginsinspect-plugin)
* [`yp-scrape plugins:install PLUGIN...`](#yp-scrape-pluginsinstall-plugin-1)
* [`yp-scrape plugins:link PLUGIN`](#yp-scrape-pluginslink-plugin)
* [`yp-scrape plugins:uninstall PLUGIN...`](#yp-scrape-pluginsuninstall-plugin)
* [`yp-scrape plugins:uninstall PLUGIN...`](#yp-scrape-pluginsuninstall-plugin-1)
* [`yp-scrape plugins:uninstall PLUGIN...`](#yp-scrape-pluginsuninstall-plugin-2)
* [`yp-scrape plugins update`](#yp-scrape-plugins-update)

## `yp-scrape hello PERSON`

Say hello

```
USAGE
  $ yp-scrape hello [PERSON] -f <value>

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

_See code: [dist/commands/hello/index.ts](https://github.com/home/hello-world/blob/v0.0.0/dist/commands/hello/index.ts)_

## `yp-scrape hello world`

Say hello world

```
USAGE
  $ yp-scrape hello world

DESCRIPTION
  Say hello world

EXAMPLES
  $ oex hello world
  hello world! (./src/commands/hello/world.ts)
```

## `yp-scrape help [COMMAND]`

Display help for yp-scrape.

```
USAGE
  $ yp-scrape help [COMMAND] [-n]

ARGUMENTS
  COMMAND  Command to show help for.

FLAGS
  -n, --nested-commands  Include all nested commands in the output.

DESCRIPTION
  Display help for yp-scrape.
```

_See code: [@oclif/plugin-help](https://github.com/oclif/plugin-help/blob/v5.1.10/src/commands/help.ts)_

## `yp-scrape plugins`

List installed plugins.

```
USAGE
  $ yp-scrape plugins [--core]

FLAGS
  --core  Show core plugins.

DESCRIPTION
  List installed plugins.

EXAMPLES
  $ yp-scrape plugins
```

_See code: [@oclif/plugin-plugins](https://github.com/oclif/plugin-plugins/blob/v2.0.11/src/commands/plugins/index.ts)_

## `yp-scrape plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ yp-scrape plugins:install PLUGIN...

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
  $ yp-scrape plugins add

EXAMPLES
  $ yp-scrape plugins:install myplugin 

  $ yp-scrape plugins:install https://github.com/someuser/someplugin

  $ yp-scrape plugins:install someuser/someplugin
```

## `yp-scrape plugins:inspect PLUGIN...`

Displays installation properties of a plugin.

```
USAGE
  $ yp-scrape plugins:inspect PLUGIN...

ARGUMENTS
  PLUGIN  [default: .] Plugin to inspect.

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Displays installation properties of a plugin.

EXAMPLES
  $ yp-scrape plugins:inspect myplugin
```

## `yp-scrape plugins:install PLUGIN...`

Installs a plugin into the CLI.

```
USAGE
  $ yp-scrape plugins:install PLUGIN...

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
  $ yp-scrape plugins add

EXAMPLES
  $ yp-scrape plugins:install myplugin 

  $ yp-scrape plugins:install https://github.com/someuser/someplugin

  $ yp-scrape plugins:install someuser/someplugin
```

## `yp-scrape plugins:link PLUGIN`

Links a plugin into the CLI for development.

```
USAGE
  $ yp-scrape plugins:link PLUGIN

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
  $ yp-scrape plugins:link myplugin
```

## `yp-scrape plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ yp-scrape plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ yp-scrape plugins unlink
  $ yp-scrape plugins remove
```

## `yp-scrape plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ yp-scrape plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ yp-scrape plugins unlink
  $ yp-scrape plugins remove
```

## `yp-scrape plugins:uninstall PLUGIN...`

Removes a plugin from the CLI.

```
USAGE
  $ yp-scrape plugins:uninstall PLUGIN...

ARGUMENTS
  PLUGIN  plugin to uninstall

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Removes a plugin from the CLI.

ALIASES
  $ yp-scrape plugins unlink
  $ yp-scrape plugins remove
```

## `yp-scrape plugins update`

Update installed plugins.

```
USAGE
  $ yp-scrape plugins update [-h] [-v]

FLAGS
  -h, --help     Show CLI help.
  -v, --verbose

DESCRIPTION
  Update installed plugins.
```
<!-- commandsstop -->
# yp-scrape
