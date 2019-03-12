# webpack-output-management-demo

## HtmlWebpackPlugin:

if we changed the name of one of our entry points, or even added a new one, the generated bundles would be renamed on a build, but our index.html file would still reference the old names

HtmlWebpackPlugin by default will generate its own index.html file, even though we already have one in the dist/ folder. This means that it will replace our index.html file with a newly generated one.

## clean-webpack-plugin

/dist folder has become quite cluttered. Webpack will generate the files and put them in the /dist folder for you, but it doesn't keep track of which files are actually in use by your project.

## run in terminal

### `npm install`

### `npm run build`

open index.html from "dist" folder