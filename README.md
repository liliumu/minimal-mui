MUI minimal boilerplate
=====

## Usage

```
npm install
npm run build # npx webpack
```

GitHub Pages --> https://liliumu.github.io/minimal-mui/

## Background

- React と MUI を使いたい
- 必要とされているツール (TypeScript, ESLint, Prettier) は導入すべき
- しかし便利という理由だけで不必要なツールは導入したくなく `npm init -y` から作りはじめて動かしたい
- 公式チュートリアルは ↑ を想定しておらず CRA や Next.js を前提としているので試行錯誤があった
- やりたいことができた & 動いたので完成とした

## Structure

- Node.js v16.x

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

## `package.json`

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
