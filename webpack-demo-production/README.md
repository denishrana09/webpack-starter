# webpack-production-demo

here we have written **separate webpack configurations** for each environment.

## webpack-merge:

With the "common" configuration in place, we won't have to duplicate code within the environment-specific configurations.

we have removed **webpack.config.js** and added **webpack.common.js**, **webpack.dev.js**, **webpack.prod.js**.

In webpack.common.js, we now have setup our entry and output configuration and we've included any plugins that are required for both environments. In webpack.dev.js, we've set mode to development. Also, we've added the recommended devtool for that environment (strong source mapping), as well as our simple devServer configuration. Finally, in webpack.prod.js,mode is set to production which loads [TerserPlugin](https://github.com/webpack-contrib/terser-webpack-plugin).

## package.json

see the changes in package.json:

~~"start": "webpack-dev-server --open",~~

```"start": "webpack-dev-server --open --config webpack.dev.js",```

~~"build": "webpack"~~

```"build": "webpack --config webpack.prod.js"```

## NODE_ENV

Technically, **NODE_ENV** is a system environment variable that Node.js exposes into running scripts. It is used by convention to determine dev-vs-prod behavior by server tools, build scripts, and client-side libraries.


## Minification

webpack v4+ will minify your code by default in production mode.

Note that while the [TerserPlugin](https://webpack.js.org/plugins/terser-webpack-plugin) is a great place to start for minification and being used by default, there are other options out there. Here are a few more popular ones:

- [BabelMinifyWebpackPlugin](https://github.com/webpack-contrib/babel-minify-webpack-plugin)
- [ClosureCompilerPlugin](https://github.com/roman01la/webpack-closure-compiler)


## run in terminal

### `npm install`

## run below given either of two commands in terminal and see the result

### `npm run start`

### `npm run build`
