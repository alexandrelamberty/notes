---
author: Alexandre Lamberty
title: NVM
description: Node version package manager
category: Package manager
tags: [package,manager,javascript,nodejs,version]
created: 2021-10-23T20:42:15+02:00
updated: 2021-10-23T20:42:15+02:00
---

# Nvm

Node version manager

## Configuration

`$NVM_DIR`

## Usage

List available version 
```bash
nvm ls-remote
nvm ls-remote | grep -i "latest"        
nvm ls-remote | grep -i "<node_version>"
```

Install version
```bash
nvm install <node_version>      // Install a specific Node version
nvm install node                // Install latest Node release (Current)
nvm install --lts               // Install latest LTS release of NodeJS
nvm install-latest-npm          // Install latest NPM release only
```

Uninstall version
```bash
nvm uninstall <node_version>    // Uninstall a specific Node version
nvm uninstall --lts             // Uninstall the latest LTS release of Node
nvm uninstall node              // Uninstall latest (Current) release of Node
```

List installed version
```bash
nvm list node                   // Lists installed Node versions
nvm list  (or)  nvm ls          // Lists installed Node versions with additional release info
```

Switch version
```bash
nvm use node                      // Switch to the latest available Node version
nvm use <node_version_or_alias>  // Switch to a specific version
nvm use --lts                    // Switch to the latest LTS Node version
```

Show version
```bash
node -v || node --version
npm -v  || npm --version
nvm -v  || nvm --version
```

Alias version
```bash
nvm alias default node                  // Always defaults to the latest available node version on a shell
nvm alias default <node_version>        // Set default node version on a shell
nvm alias <alias_name> <node_version>   // Set user-defined alias to Node versions 

nvm unalias <alias_name>                // Deletes the alias named <alias_name>
```

Path to version executable
```bash
nvm which <installed_node_version>      // path to the executable where a specific Node version is installed
```

Uninstall Nvm
```bash
To remove, delete, or uninstall nvm, just remove the $NVM_DIR folder (usually ~/.nvm)
```
## Usage

## References

- [](https://gist.github.com/chranderson/b0a02781c232f170db634b40c97ff455)
