# eslint-plugin-fsd-path-import

plugin for correct fsd imports

## Installation

You'll first need to install [ESLint](https://eslint.org/):

```sh
npm i eslint --save-dev
```

Next, install `eslint-plugin-fsd-path-import`:

```sh
npm install eslint-plugin-fsd-path-import --save-dev
```

## Usage

Add `fsd-path-import` to the plugins section of your `.eslintrc` configuration file. You can omit the `eslint-plugin-` prefix:

```json
{
    "plugins": [
        "fsd-path-import"
    ]
}
```


Then configure the rules you want to use under the rules section.

```json
{
    "rules": {
      "fsd-path-import/path-checker": ["error", { "alias": "@" }],
      "fsd-path-import/public-api-imports": ["error", { "alias": "@", "testFilesPatterns": [ "**/test.ts" ]  }],
      "fsd-path-import/layer-imports": [
        "error",
        { "alias": "@", "ignoreImportPatterns": ["**/StoreProvider"] }
      ]
    }
}
```



