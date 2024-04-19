# Easier Apis
![CC BY-SA 4.0](https://img.shields.io/badge/CC-BY--SA%204.0-blue?logo=CreativeCommons)
![Node.js v18.17.0^](https://img.shields.io/badge/node.js-18.17.0^-darkgreen?logo=nodedotjs)
![Exoress 4.19.0^](https://img.shields.io/badge/express-4.19.0^-orange?logo=express)
### By Anthony Maxwell

## Table of Contents
- [Introduction](#introduction)
- [Requirements](#requirements)
- [Installation Guide](#installation-guide)
- [Usage](#usage)
- [FAQ](#faq)
- [License](#license)

## Introduction
Easier APIs is a platform based on express that allows you to make apis easily.

## Requirements
- Node.js 18.17.0 or above
- Express 4.19.0 or above
- Multer 2.0.0-rc.1 or above

## Installation Guide
```npm install easier-apis```: It's that simple.

## Usage
Easier Apis is based on the library express, and uses multer for file managment.
Begin by importing Easier Apis and Express: 
```javascript
const easierApis = require('easier-apis');
const express = require('express');
```

Initialize an application and api for both:
```javascript
const app = express();
const api = easierApis();
```

Now, link the express app to the api.
```javascript
api.attach(app);
```

You are now attached, and can use the api!

You can setup an enpoint by calling the endpoint function as follows:
```javascript
api.endpoint({ url: "/endpoint/:parameter" }, (req, res, params) => {
    res.send(`you entered the parameter: ${params.parameter}`);
});
```

You will need to run the express app as normal:
```javascript
app.listen(3000, () => console.log('Server running on port 3000'));
```

## FAQ (Frequently Asked Questions)
There is currently no FAQs, as this is the first version. Submit issues on the github, and questions on Stack Overflow or other sites tagged #easierApis

## License
![CC BY-SA 4.0](https://img.shields.io/badge/CC-BY--SA%204.0-blue?logo=CreativeCommons)
<p xmlns:cc="http://creativecommons.org/ns#" xmlns:dct="http://purl.org/dc/terms/"><a property="dct:title" rel="cc:attributionURL" href="http:///https://www.npmjs.com/package/easier-apis">Easier Apis</a> by <span property="cc:attributionName">Anthony Maxwell</span> is licensed under <a href="https://creativecommons.org/licenses/by-sa/4.0/?ref=chooser-v1" target="_blank" rel="license noopener noreferrer" style="display:inline-block;">CC BY-SA 4.0<img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/cc.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/by.svg?ref=chooser-v1" alt=""><img style="height:22px!important;margin-left:3px;vertical-align:text-bottom;" src="https://mirrors.creativecommons.org/presskit/icons/sa.svg?ref=chooser-v1" alt=""></a></p>
You are free to:

- Share: copy and redistribute the material in any medium or format for any purpose, even commercially.
- Adapt: remix, transform, and build upon the material for any purpose, even commercially.
The licensor cannot revoke these freedoms as long as you follow under the following license terms:
- Attribution: You must give appropriate credit , provide a link to the license, and indicate if changes were made . You may do so in any reasonable manner, but not in any way that suggests the licensor endorses you or your use.
- ShareAlike: If you remix, transform, or build upon the material, you must distribute your contributions under the same license as the original.
- You may not apply legal terms or technological measures that legally restrict others from doing anything the license permits.
- No warranties are given. The license may not give you all of the permissions necessary for your intended use. For example, other rights such as publicity, privacy, or moral rights may limit how you use the material.