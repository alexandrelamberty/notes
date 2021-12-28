---
author: Alexandre Lamberty
title: NPM
description: | 
 Package manager for the JavaScript programming language and runtime
 environment Node.js
category: Package manager
tags: ["package","manager","javascript","nodejs"]
created: 2021-10-23T20:42:15+02:00
updated: 2021-10-23T20:42:15+02:00
---
# NPM

Node Package Manager

## Config

## CLI

## Using package

## Registry

## Github

### Public

```shell
npm i https://github.com/user_name/node_project_name
```

```json
"package-name": "https://github.com/<user>/<repo>.git"
```

### Private

#### Https and oauth

You will need to have or create an access token with permissions to access the repository. see: [Github - Managing deploy keys][link text itself]

```json
"package-name": "git+https://<github_token>:x-oauth-basic@github.com/<user>/<repo>.git"
```

#### Ssh

You will need to create an ssh key. see:

```shell
npm install git+ssh://git@github.com:user_name/node_project.git
```

```json
"package-name": "git+ssh://git@github.com:<user>/<repo>.git"
```

## References

- [npm Docs](https://docs.npmjs.com/)
- [Managing deploy keys](https://docs.github.com/en/developers/overview/managing-deploy-keys)
- [Connecting to github with ssh](https://docs.github.com/en/authentication/connecting-to-github-with-ssh)
- [Creating a token
  Using a token on the command line
  Further reading
  Creating a personal access token](https://docs.github.com/en/authentication/keeping-your-account-and-data-secure/creating-a-personal-access-token)
