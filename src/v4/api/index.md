---
title: API
type: api
---

# API

## Everflow Configuration File

The configuration file is called `evconfig.json` containing Everflow's global configurations. You can modify its properties listed below before bootstrapping your application:

Placement is next to your main.ts file in your root src folder.

### routerMode

- **Type:** `RouterMode`

- **Values:** `hash` | `history`

- **Usage:**

Tells Everflow to use hash or history routing with Vue Router

  ``` json
  {
    "routerMode": "hash", //or history
  }
  ```

### mountId

Tells Everflow what HTML ID to mount the Vue Router

- **Type:** `string`

- **default:** `app`

- **Usage:**

  ``` json
  {
    "mountId": "app",
  }
  ```

### apiURL

Tells Everflow what your API entry point is

- **Type:** `string`

- **default:** `https://api.localhost`

- **Usage:**

  ``` json
  {
    "apiURL": "https://api.localhost",
  }
  ```

### i18n

I18n information for your application

- **Type:** `object`

- **Usage:**

  ``` json
  {
    "i18n": {
        "enabled": <boolean>,
        "defaultLocale": "<i18n locale>",
        "fallbackLocale": "<i18n locale>",
        "modules": <boolean>
    },
  }
  ```

### i18n / Options

#### enabled
Enables i18n loading in application

- **Type:** `boolean`

- **default:** `true`

- **Usage:**

  ``` json
  {
    "enabled": true,
  }
  ```

#### defaultLocale
The default i18n locale

- **Type:** `string`

- **default:** `en`

- **Usage:**

  ``` json
  {
    "defaultLocale": "en",
  }
  ```

#### fallbackLocale
The fallback locale for if the default locale fails. `user` is a custom type to Everflow and will detect the users browsers language.

- **Type:** `string`

- **default:** `en`

- **values:** `i18n-locale` | `user`

- **Usage:**

  ``` json
  {
    "fallbackLocale": "en",
  }
  ```

#### modules
I18n with modules enabled keeps all locales modules separated

- **Type:** `boolean`

- **default:** `true`

- **details:** `true`

IF `true` all translations must start with a module name unless stored in the root i18n folder.
$t('<module_name>.message.hello')

    IF `false` all translations merge and will overwrite from each module.
    $t('message.hello')

- **Usage:**

  ``` json
  {
    "modules": true,
  }
  ```

### security

Security information for your application

- **Type:** `object`

- **Usage:**

  ``` json
  {
    "security": {
        "key": "<256-bit-key>"
    }
  }
  ```

### security / Options

#### key
A 256 bit key for AES encryption, generated if installed Everflow via Vue Cli 3

- **Type:** `string`

- **default:** `<installation-generated>`

- **Usage:**

  ``` json
  {
    "key": "<256-bit-key>",
  }
  ```

### storage

Security information for your application

- **Type:** `object`

- **Usage:**

  ``` json
  {
    "storage": {
        "name": "<storage-name>",
        "driver": [],
        "size": <storage-size-in-bytes>,
        "storeName": "<storage-name>"
    }
  }
  ```

### security / Options

TODO...

### datetime

Date and time information for your application

- **Type:** `object`

- **Usage:**

  ``` json
  {
    "datetime": {
        "date": {
            "format": "<date_format>"
        },
        "time": {
            "format": "<time_format>"
        }
    }
  }
  ```

#### date
Moment.js date serialization format. Formats [here](https://momentjscom.readthedocs.io/en/latest/moment/01-parsing/03-string-format/)

- **Type:** `string`

- **default:** `YYYY-MM-DD`

- **Usage:**

  ``` json
  {
    "fallbackLocale": "YYYY-MM-DD",
  }
  ```

#### time
Moment.js time serialization format. Formats [here](https://momentjscom.readthedocs.io/en/latest/moment/01-parsing/03-string-format/)

- **Type:** `string`

- **default:** `HH:mm:ss`

- **Usage:**

  ``` json
  {
    "fallbackLocale": "HH:mm:ss",
  }
  ```




