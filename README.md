https://medium.com/@menezes.carlos/angular-2-setting-up-your-working-environment-52b985d1d341#.12dyylk59
How to make setup?
1. npm init
2. npm install angular2 --save
3. npm install systemjs --save
4.npm install tsc --save
5. Creating tsconfig.json (try this with tsc --init)
#npm install -g typescript (node shoud be above 4)
#tsc --init --target es5 --sourceMap --experimentalDecorators --emitDecoratorMetadata

6. Creating typings.json and add below
{
  "ambientDependencies":
  {
    "es6-shim": "github:DefinitelyTyped/DefinitelyTyped/es6-shim/es6-shim.d.ts#6697d6f7dadbf5773cb40ecda35a76027e0783b2"
  }
}


7. npm install typings --save-dev
8. npm install concurrently --save-dev
9. npm install lite-server --save-dev

Add following scripts to package.json
"scripts": {
    "postinstall": "npm run typings install",
    "tsc": "tsc",
    "tsc:w": "tsc -w",
    "lite": "lite-server",
    "app": "concurrent \"npm run tsc:w\" \"npm run lite\" ",
    "typings": "typings"
 }



2. create systemjs.config.js
https://angular.io/docs/ts/latest/guide/deployment.html
