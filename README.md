# React-app

## React 実行

- React インストール

```
npm install --save react react-dom
```

- webpack インストール

```
npm install webpack@beta -g
```

```
npm install --save-dev webpack
```

- Babel インストール

```
npm install --save-dev babel-loader babel-core babel-preset-es2015 babel-preset-react
```

- babel ファイル設定

```
touch .babelrc
```

```
open .babelrc
```

```
{ "presets": ["react", "es2015"] }
```

- webpack 設定

```
touch webpack.config.js
```

```
open webpack.config.js
```

```
module.exports = {
  entry: './src/index.js',
  output: {
    path: './dist',
    filename: 'bundle.js'
  },
  module: {
    loaders: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        loader: 'babel-loader'
      }
    ]
  }
}
```

- package.json に以下を設定

```
"scripts": {
    "test": "echo \"Error: no test specified\" && exit 1",
    "build": "webpack",
    "start": "webpack-dev-server --hot --inline"
  }
```

- webpack の実行

```
npm run build
```

- 自動リロード

```
npm start
```
