# Alpha Commits

### Quickstart para trabalhar com commits enriquecidos.

<b>Execute no terminal os seguintes comandos:</b>

```
yarn global add commitizen rimraf conventional-recommended-bump conventional-changelog-cli conventional-github-releaser conventional-commits-detector json

commitizen init cz-conventional-changelog --save-dev --save-exact

yarn add --dev husky conventional-changelog validate-commit-msg
```

<b>ou</b>

```
npm global add commitizen rimraf conventional-recommended-bump conventional-changelog-cli conventional-github-releaser conventional-commits-detector json

commitizen init cz-conventional-changelog --save-dev --save-exact

yarn add --dev husky conventional-changelog validate-commit-msg
```

<b>Edite o package.json:</b>

```sh
 {
    "scripts": {
      "commitmsg": "validate-commit-msg"
    }
  }
  ```
  
  <b>Já na raiz do arquivo package.json coloque as seguintes coisas:</b>
  
  ```sh
  "config": {
    "validate-commit-msg": {
      "types": [
        "feat",
        "fix",
        "docs",
        "style",
        "refactor",
        "perf",
        "test",
        "chore",
        "revert",
        "ci",
        "build"
      ],
      "warnOnFail": false,
      "maxSubjectLength": 100,
      "subjectPattern": ".+",
      "subjectPatternErrorMsg": "subject does not match subject pattern!",
      "helpMessage": ""
    },
    "commitizen": {
      "path": "./node_modules/cz-conventional-changelog"
    }
 }
  ```
