Here’s a **Webpack / Build Tools** cheat sheet with an index to guide you through the key configurations, loaders, plugins, and basic setup.

````markdown
# Webpack / Build Tools Cheat Sheet

## Index

## 1. Basic Webpack Setup

### Installing Webpack

```bash
npm install --save-dev webpack webpack-cli
```
````

### Basic Webpack Configuration

Create a `webpack.config.js` file:

```js
const path = require('path');

module.exports = {
  entry: './src/index.js',
  output: {
    filename: 'bundle.js',
    path: path.resolve(__dirname, 'dist'),
  },
  mode: 'development',  // or 'production'
};
```

### Entry & Output

- **Entry**: Specifies the entry point for your app (default is `src/index.js`).
- **Output**: Defines where the bundled file is placed.

### Development Mode vs Production Mode

- **Development Mode**: Easier debugging, no minification, includes detailed error messages.
- **Production Mode**: Minified code, optimized for speed and smaller bundle size.

---

## 2. Loaders

Webpack loaders allow you to preprocess files as they are bundled.

### CSS Loader

```bash
npm install --save-dev style-loader css-loader
```

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.css$/,
        use: ['style-loader', 'css-loader'],
      },
    ],
  },
};
```

### Babel Loader

For transpiling ES6+ JavaScript into older versions:

```bash
npm install --save-dev babel-loader @babel/core @babel/preset-env
```

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.js$/,
        exclude: /node_modules/,
        use: {
          loader: 'babel-loader',
          options: {
            presets: ['@babel/preset-env'],
          },
        },
      },
    ],
  },
};
```

### File Loader

For managing files like fonts and media:

```bash
npm install --save-dev file-loader
```

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.(png|jpg|gif)$/,
        use: ['file-loader'],
      },
    ],
  },
};
```

### Image Loader

For optimizing images:

```bash
npm install --save-dev image-webpack-loader
```

```js
module.exports = {
  module: {
    rules: [
      {
        test: /\.(png|jpe?g|gif)$/,
        use: [
          'file-loader',
          {
            loader: 'image-webpack-loader',
            options: {
              mozjpeg: {
                progressive: true,
                quality: 65,
              },
              optipng: {
                enabled: false,
              },
              pngquant: {
                quality: [0.65, 0.90],
                speed: 4,
              },
            },
          },
        ],
      },
    ],
  },
};
```

---

## 3. Plugins

### HTML Webpack Plugin

Automatically generates an HTML file for your bundle:

```bash
npm install --save-dev html-webpack-plugin
```

```js
const HtmlWebpackPlugin = require('html-webpack-plugin');

module.exports = {
  plugins: [
    new HtmlWebpackPlugin({
      template: './src/index.html',
    }),
  ],
};
```

### Mini CSS Extract Plugin

Extracts CSS into separate files for production:

```bash
npm install --save-dev mini-css-extract-plugin
```

```js
const MiniCssExtractPlugin = require('mini-css-extract-plugin');

module.exports = {
  plugins: [
    new MiniCssExtractPlugin({
      filename: '[name].[contenthash].css',
    }),
  ],
};
```

### Clean Webpack Plugin

Cleans the `dist/` folder before each build:

```bash
npm install --save-dev clean-webpack-plugin
```

```js
const { CleanWebpackPlugin } = require('clean-webpack-plugin');

module.exports = {
  plugins: [new CleanWebpackPlugin()],
};
```

### Define Plugin

Define global constants for use during build time:

```js
const webpack = require('webpack');

module.exports = {
  plugins: [
    new webpack.DefinePlugin({
      'process.env.NODE_ENV': JSON.stringify('production'),
    }),
  ],
};
```

---

## 4. Webpack Dev Server

### Setting up Dev Server

```bash
npm install --save-dev webpack-dev-server
```

```js
module.exports = {
  devServer: {
    contentBase: './dist',
    port: 8080,
  },
};
```

### Hot Module Replacement (HMR)

Enables updating modules without refreshing the entire page:

```bash
npm install --save-dev webpack webpack-cli webpack-dev-server
```

```js
module.exports = {
  devServer: {
    contentBase: './dist',
    hot: true,
  },
  plugins: [
    new webpack.HotModuleReplacementPlugin(),
  ],
};
```

---

## 5. Optimization

### Code Splitting

Split code into smaller bundles for better performance:

```js
module.exports = {
  optimization: {
    splitChunks: {
      chunks: 'all',
    },
  },
};
```

### Tree Shaking

Remove unused code in your project:

```js
module.exports = {
  mode: 'production',
  optimization: {
    usedExports: true,
  },
};
```

### Minification

For JS minification in production:

```bash
npm install --save-dev terser-webpack-plugin
```

```js
const TerserPlugin = require('terser-webpack-plugin');

module.exports = {
  optimization: {
    minimize: true,
    minimizer: [new TerserPlugin()],
  },
};
```

---

## 6. Module Resolution

### Alias Configuration

Shorten import paths with aliases:

```js
module.exports = {
  resolve: {
    alias: {
      Components: path.resolve(__dirname, 'src/components/'),
    },
  },
};
```

### Extensions

Resolve certain file types without specifying their extensions:

```js
module.exports = {
  resolve: {
    extensions: ['.js', '.jsx', '.json'],
  },
};
```

---

This cheat sheet provides the essentials for getting started with Webpack and customizing your build process.

This will give you a structured and easy-to-navigate cheat sheet for Webpack.
