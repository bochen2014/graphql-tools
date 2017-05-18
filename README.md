# publish a npm package
## login to npm via `npm adduser`
>if username exists, login; otherwise signup
$ npm adduser --registry=https://registry.npmjs.org
Username: bochen2014
Password: Op*\*do\*0*
Email: (this IS public) bochen2014@yahoo.com
Logged in as bochen2014 on https://registry.npmjs.org/.
## make sure you have `prepublish` defined

 ```
 package.json
 {
    "prepublish": "tsc",

    "main": "dist/index.js",  // only this file ,along with its referenced file**S**, are uploaded


 }


tsconfig.json
{
  	"rootDir": "./src",
		"outDir": "./dist",
}
 ```

## run `npm publish --registry=https://registry.npmjs.org`
```
$ npm publish --registry=https://registry.npmjs.org

> graphql-tools-bchen@0.11.0 prepublish D:\graphql-tools
> npm run compile


> graphql-tools-bchen@0.11.0 compile D:\graphql-tools
> tsc

+ graphql-tools-bchen@0.11.0
```
