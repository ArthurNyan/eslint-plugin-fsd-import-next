# eslint-plugin-fsd-import-next

Plugin for checking imports path in [FSD](https://feature-sliced.design/) project.

## Installation

You'll first need to install [ESLint](https://eslint.org/):

```sh
npm i eslint --save-dev
```

Next, install `eslint-plugin-fsd-import-next`:

```sh
npm install eslint-plugin-fsd-import-next --save-dev
```

## Usage

Add `fsd-import` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
    "plugins": [
        "fsd-import"
    ]
}
```


Then configure the rules you want to use under the rules section.

```json
{
    "rules": {
        "fsd-import-next/fsd-relative-path": "error",
        "fsd-import-next/public-api-imports": "error",
        "fsd-import-next/layer-imports": "error",
    }
}
```

## Supported Rules
Check FSD imports is correct:
* [fsd-relative-path](https://github.com/ArthurNyan/eslint-plugin-fsd-import-next/blob/main/docs/rules/fsd-relative-path.md)
 Imports within one slice should be relative.
* [public-api-imports](https://github.com/ArthurNyan/eslint-plugin-fsd-import-next/blob/main/docs/rules/public-api-imports.md)
Absolute imports should be only from public API.
* [layer-imports](https://github.com/ArthurNyan/eslint-plugin-fsd-import-next/blob/main/docs/rules/layer-imports.md)
Modules on one layer can only interact with modules from the layers strictly below.


