# New Project (WordPress)
New Wordpress Project setup instructions for _Newbs_!
## Initial One Time Setup:
1. Make sure you have Node.js setup on your system.
2. Install Grunt CLI globally on your system:  
`sudo npm install -g grunt-cli`

## 1: Create New Repository
First [create a new repositoty](https://help.github.com/articles/creating-a-new-repository/) on github.


## 2: Folder Structure
On your local machine create your new project folder in your `Sites` directory and setup the following folder structure inside it:
- Builds
 - Development
 - Production
- Components
 - Sass
 - Scripts
 
## 3: Setup package.json
 Setup package.json by running the following command in terminal:  
```npm init```

- name: projectname //projct name is all one word, lowercased.
- version: 1.0.0
- description: Project description here.
- entry point: index.php
- git repository: //github link.
- keywords: wordpress
- author: The Gigawatt Group \<info@gigawattgroup.com\>
- license : //accept default.

Review and Accept the changes you just made. Go inside the `package.json` file and remove up any unwanted parts.

## 4: Setup Gruntfile.js
1. Create a file in your project folder called `Gruntfile.js` and use the example provided in this repo.
2. Install grunt in your project folder:  
`npm install grunt --save-dev`
3. Install all required packages:    
```npm install grunt-contrib-concat --save-dev  
npm install grunt-contrib-uglify --save-dev  
npm install grunt-contrib-watch --save-dev  
npm install grunt-autoprefixer --save-dev  
npm install grunt-sass --save-dev```
