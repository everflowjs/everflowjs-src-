---
title: Introduction
type: guide
order: 2
---


# Introduction

## What is Everflow?

Everflow is a **batteries included** framework for building enterprise grade front-end applications with TypeScript and Vue.js.

Scalibity defined: `The capacity to be changed in size or scale` and containerizing code is key to this. Why develop code multiple times when you can just re-use it, and modularbility is key here.

## Getting Started

<a class="button" href="installation.html">Installation</a>

<p class="tip">The official guide assumes basic level knowledge of vue.js and Vue CLI tools. If you are totally new to vue.js development, it might help to understand the basics of vue.js such as virtual DOM, routes, and component’s.</p>

> Yarn is our recommended npm package tool and will be used in this documentation. [Get it now](https://classic.yarnpkg.com/en/docs/install)
> Vue CLI 3 will be used in this documentation. [Get it now](https://cli.vuejs.org/guide/installation.html)

##### Vue CLI 3 Yarn Install
``` bash
$ yarn global add @vue/cli
```

### Create Everflow Project
The easiest and recommended way to get started with Everflow is with Vue CLI 3:

#### Step 1 - Create new vue project
``` bash
# replace <app-name> with your app name
$ vue create <app-name>
```

##### Console Choices:
``` text
- babel (required)
    - Use Babel alongside TypeScript: **Yes**
- TypeScript (required)
    - Use class-style component syntax: **Yes**
- Router  (required)
    - Use history mode for router: **Your Choice**
- Vuex (required)
- CSS Pre Processors (optional) - *However recommended.*
    - Pick a CSS pre-processor: **(node-sass) - recommended**
- Progressive Web App (optional) - *However recommended.*
- Linter
    - Pick a linter|formatter config: **Basic/Your Choice**
    - Pick additional lint features: **Lint on save/Your Choice**
- Config Files
    - Where do you prefer placing config? **In dedicated config files**
```

#### Step 2 - Open new Vue app directory
``` bash
# replace <app-name> with your app name
$ cd <app-name>
```

#### Step 3 - Add everflow vue plugin
``` bash
$ vue add vue-cli-plugin-everflow
```

<p class="tip">If you run this command on an existing project save your work. This will overwrite your main.ts file, with the possibility of others.</p>

##### Console Choices:
``` text
- Vue Router routing mode?: **Choice**
    • This is the routing mode for Vue Router
- What is the root API URL for your server?: **Choice**
    • The base url for your API entry points. e.g. (https://api.example.org/)
- Default i18n locale for app(...)?: **Choice**
    • `user` tells everflow to use the users browser language
    • i18n support locale
- Fallback locale, if default fails?: **Choice**
    • If `user` or default locale fails, use a fallback option
    • i18n support locale
    • Recommended to be your native apps language
- Date util class serialize format?: **Choice**
    • Everflow uses moment.js to serialize dates. This is the format.
- Time util class serialize format?: **Choice**
    • Everflow uses moment.js to serialize times. This is the format.
- Enable i18n loading in your project?: **Choice**
    • This will enable the locale options and create i18n folders in project
- Delete orphaned files from VueJS example project?: **Choice**
    • Will remove un-linked files created from "vue create <app-name>" command
```

#### Step 4 - Running Everflow
``` bash
$ yarn serve
```