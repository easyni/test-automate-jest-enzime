# README
⚠️ ⚠️ ⚠️ 
this project is WIP.
⚠️ ⚠️ ⚠️ 
## Basic install & use
### node version 8

this project have the objective to create automatically test files with template bases.

### HOW TO USE

just install npx globaly

 
```bash 

npm install -g npx

```
and launch: 
 
```bash 

npx git+https://github.com/easyni/test-automate-jest-enzyme.git

```

you can add your own processors in addition to existing ones with an .testautomaterc

```json
{
  "tests": [
    {
      "name": "component",
      "label": "component (jest enzyme)",
      "processFile": "./lib/process/componentProcess.js"
    },
    {
      "name": "function",
      "label": "function (jest )",
      "processFile": "./lib/process/functionProcess.js"
    },
    {
      "name": "reducer",
      "label": "reducer (jest)",
      "processFile": "./lib/process/reducerProcess.js"
    },
    {
      "name": "action-redux",
      "label": "action redux (jest)",
      "processFile": "./lib/process/actionProcess.js"
    }
  ]
}
```

  **name** > must be an unique key
  
  **label** > label is displayed during the information collect
   
  **processFile** > the process file will parse all yours files, and generate your test file.

 ⚠️ ⚠️ ⚠️ 
 
 processFile must export a function named **processFiles** as 
 
 ```js

export const processFiles = ({filePath, fileName}) => {
    //... do what you want
}
 ```