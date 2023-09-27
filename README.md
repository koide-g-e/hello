# hello

helloworld and my eslint, prettier config

```shell
% npm i --save-dev eslint \
    prettier \
    @typescript-eslint/eslint-plugin \
    @typescript-eslint/parser \
    eslint-config-prettier
```

.prettierrc.json

```json
{
  "printWidth": 120,
  "tabWidth": 2,
  "semi": true,
  "quoteProps": "preserve"
}
```

.eslintrc.json

```json
{
  "env": {
    "browser": true,
    "es2021": true,
    "node": true
  },
  "extends": ["eslint:recommended", "prettier", "prettier/@typescript-eslint", "plugin:@typescript-eslint/recommended"],
  "parser": "@typescript-eslint/parser",
  "parserOptions": {
    "ecmaVersion": "latest",
    "sourceType": "module"
  },
  "plugins": ["@typescript-eslint"],
  "rules": {
    "semi": ["error", "always"],
    "quotes": ["error", "double"]
  },
  "root": true
}
```

vscode settings.json

```json
"editor.formatOnSave": true,
"editor.formatOnPaste": true,
"editor.formatOnType": true,
"editor.defaultFormatter": "esbenp.prettier-vscode",
"editor.codeActionsOnSave": {
  "source.fixAll.eslint": true
}

```
