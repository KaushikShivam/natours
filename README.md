# Natours - Outdoor is where life happens


[Natours](https://rawcdn.githack.com/KaushikShivam/natours/4689e752942b08a178655c7be225171b52959389/index.html) | Exciting tours for adventurous people

Natours is a professional and modern responsive website tempate for the Travel industry. The template can be used for apps such as Travel blogs, Tour bookings and more.

![Natours Screenshot](screenshot.png)

## Table of content
- [Description](#description)
- [Installation](#installation)
- [Scripts](#scripts)
- [Contact](#contact)



## Description
This template uses the following:
- ### Modern CSS 
  - ```clip-path```
  - ```keyframes animations```
  - ```background-clip```
  - ```backface-visibility```
  - ```background video```
  - ```pop up using pure css```
- ### BEM Methodology 
- ### Custom 4 column grid
- ### SASS
  - ```variables```
  - ```nesting```
  - ```parials and imports```
  - ```mixins```
  - ```functions```
  - ```extends```
- ### 7-1 project structure for SASS Files - 
  - ```base/```
  - ```components/```
  - ```layout/```
  - ```pages/```
  - ```themes/```
  - ```abstracts/```
  - ```vendors/```
  
A [build script](#scripts) is created to accomodate older browser compatibility
  

## Installation

1. Clone the project to your local directory
```
git clone https://github.com/KaushikShivam/natours.git
```

2. The project uses NPM for managing dependencies. Run npm install to install all the required dependencies
```
npm install
```
3. Run the watch script to view live changes to your CSS
```
npm run watch:sass
```
4. Open the index.html file in your browser to view the website in all its glory (Live-server is recommended to view live changes automatically)


## Scripts
The project uses [AutoPrefixer](https://github.com/postcss/autoprefixer), [Node-sass](https://github.com/sass/node-sass), [npm-run-all](https://www.npmjs.com/package/npm-run-all) etc to build the following scripts:

### Watch live changes in development
1. Watch live changes to the sass
```
"watch:sass": "node-sass sass/main.scss css/style.css -w"
```

2. Run Live-server for live development changes
```
"devserver": "live-server --browser=firefox"
```
3. Script to run both simultaneously
```
"start": "npm-run-all --parallel devserver watch:sass"
```

Run ```npm start``` to run the script

### Build script for production

1. Compile sass files
```
"compile:sass": "node-sass sass/main.scss css/style.comp.css"
```

2. Concat all the css files including font styles etc
```
"concat:css": "concat -o css/style.concat.css css/icon-font.css css/style.comp.css",
```

3. Add prefixes automatically to the modern CSS rules (supports last 10 years - Can be configured)
```
"prefix:css": "postcss --use autoprefixer -b 'last 10 versions' css/style.comp.css -o css/style.prefix.css"
```

4. Adds compression
```
"compress:css": "node-sass css/style.prefix.css css/style.css --output-style compressed"
```
5. Final Build process
```
"build:css": "npm-run-all compile:sass concat:css prefix:css compress:css"
```

Run ```npm run build:css``` to run the build script

## Contact
You can contact me at:

- [Portfolio](https://www.shivamkaushik.com)
- [Email](mailto:shivamkaushikofficial@gmail.com)
- [Linkedin](https://www.linkedin.com/in/kshivamdev/)
- [Twitter](https://twitter.com/kShivamDev)
- [Medium](https://medium.com/@shivamkaushikofficial)
- [Angellist](https://angel.co/kshivamdev)



