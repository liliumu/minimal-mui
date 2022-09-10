Minimal MUI Boilerplate
=====

GitHub Pages - https://liliumu.github.io/minimal-mui/

## 使い方

```
npm install
npm run build # npx webpack
```

## 背景

- React と MUI を使いたい
- `npm init -y` から作り始めたい
- 必要なものは導入したいが (便利という理由だけで) 不必要なものを導入したくない

## 構成

- Node.js v18.7.0

```
.
├── .gitignore
├── package.json
├── pages
│   └── index.html
├── src
│   └── index.tsx
├── tsconfig.json
└── webpack.config.js
```

## `package.json` について

### dependencies

- MUI
- React
- ReactDOM

```
  "dependencies": {
    "@emotion/react": "^11.10.4",  // React
    "@emotion/styled": "^11.10.4", // MUI
    "@mui/material": "^5.10.4",    // MUI
    "react-dom": "^18.2.0"         // ReactDOM
  },
```

### dev dependencies

- 2022 年、導入されやすい 3 点 -> `typescript` `eslint` `prettier`
- dependencies　をバンドルするために -> `webpack` `webpack-cli`
- Webpack が .ts .tsx をバンドルするために -> `ts-loader`
- ReactDOM は JS で書かれているため型定義が必要 -> `@types/react-dom`

```
  "devDependencies": {
    "@types/react-dom": "^18.0.6", // ReactDOM の型定義
    "eslint": "^8.23.0",           // ESLint
    "prettier": "^2.7.1",          // Prettier
    "typescript": "^4.8.3",        // TypeScript
    "webpack": "^5.74.0",          // Webpack
    "webpack-cli": "^4.10.0"       // Webpack CLI
    "ts-loader": "^9.3.1",         // TypeStrong/ts-loader
  }
```
