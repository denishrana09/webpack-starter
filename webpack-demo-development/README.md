# webpack-development-demo

## inline-source-map:

if you bundle three source files (a.js, b.js, and c.js) into one bundle (bundle.js) and one of the source files contains an error, the stack trace will simply point to bundle.js. This isn't always helpful as you probably want to know exactly which source file the error came from.

JavaScript offers source maps, which maps your compiled code back to your original source code. If an error originates from b.js, the source map will tell you exactly that.

(try to generate some error, ex. write console.log of print.js erroneous, then start server and see the console)

## webpack --watch:

You can instruct webpack to "watch" all files within your dependency graph for changes. If one of these files is updated, the code will be recompiled so you don't have to run the full build manually.

## webpack-dev-server:

after using "webpack --watch", all changed files will be recompiled to build but still you have to reload index.html file.

The webpack-dev-server provides you with a simple web server and the ability to use live reloading.

## webpack-dev-middleware:

webpack-dev-middleware is a wrapper that will emit files processed by webpack to a server. This is used in webpack-dev-server internally.

after "server.js" file added, you don't need to use "npm run start", you have to write "npm run server".

Now fire up your browser and go to http://localhost:3000. You should see your webpack app running and functioning!

## run in terminal

### `npm install`

### `npm run watch`

## run in different terminal

### `npm run server`
