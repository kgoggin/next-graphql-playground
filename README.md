# next-graphql-playground

I created this repo as an example of the [issue I filed here](https://github.com/graphcool/graphql-playground/issues/165#issuecomment-336992718) - graphql-playground tries to `require` .svg files in its code, and Next.js doesn't know how to handle those.

## Running the app

Clone it, `yarn install`, then run `yarn dev` to boot it up. https://localhost:3000 should work fine, but http://localhost:3000/graphql-playground will generate errors when Next.js tries to build that route:

```
Module parse failed: /Users/agoggin/www/vhosts/next-graphql-playground/node_modules/codemirror/lib/codemirror.css Unexpected token (3:0)
You may need an appropriate loader to handle this file type.
| /* BASICS */
|
| .CodeMirror {
|   /* Set height, width, borders, and global font properties here */
|   font-family: monospace;

 @ ./node_modules/graphql-playground/lib/components/CodeGenerationPopup/CodeGenerationPopupCode.js 39:8-48
 @ ./node_modules/graphql-playground/lib/components/CodeGenerationPopup/CodeGenerationPopup.js
 @ ./node_modules/graphql-playground/lib/components/Playground.js
 @ ./node_modules/graphql-playground/lib/lib.js
 @ ./pages/graphql-playground.js?entry
 @ multi ./pages/graphql-playground.js?entry
 ```
