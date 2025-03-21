>Code Step By Step

# Nodejs is --> async and single threaded

> Use nodemon package for live reloading purpose. install it globaly

## Ways to run the node js programs 
* node ---> for using command line scripting
* node <filename.js> --> using files

> For importing file use require()
  >> for ex: const user = require('./user.js');
> For export use module.export()

# Core modules (Non-Global modules) & Global modules
## Core Modules:
* Compulsory we need to import them

> 
* fs
* http 
* path
* OS module
  
## Global Modules:
* Are the one no need to import, Directly we can use them.
   For ex: console.log();
*


***
```js
const fs = require('fs');
//It's better to import only the specific function rather than importing entire module as mentioned above
const fs = require('fs').writeFileSync;
```
## How node js works
![How NodeJs works!](./images/Screenshot%202025-03-20%20212229.png "How NodeJs Works")

## Express Js
## Middleware
## MongoDB
## Mongoose
## Search API
## Upload File  *--> Multer