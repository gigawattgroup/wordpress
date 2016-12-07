# New Project (WordPress)
New Wordpress Project setup instructions for _Noobs_!
## Initial One Time Setup:
1. Make sure you have Node.js setup on your system.

2. Install Grunt CLI globally on your system:  
`sudo npm install -g grunt-cli`

3. Install Bower globally on your system:  
`sudo npm install -g bower`

## 1: Create New Repository
First [create a new repositoty](https://help.github.com/articles/creating-a-new-repository/) on github.

## 2: Create Project .gitignore file
Use a gitignore template specific to your project or have one auto populated from [gitignore.io](https://www.gitignore.io/).

## 3: Folder Structure
On your local machine create your new project folder in your `Sites` directory and setup the following folder structure inside it:
- builds
 - development
 - production
- components
 - sass
 - scripts
 
## 4: Setup package.json
 Setup package.json by running the following command in terminal:  
```npm init```

- name: projectname *projct name is all one word, lowercased.*
- version: 1.0.0
- description: Project description here.
- entry point: index.php
- git repository: *github link.*
- keywords: wordpress
- author: The Gigawatt Group \<info@gigawattgroup.com\>
- license : *accept default.*

Review and Accept the changes you just made. Go inside the `package.json` file and remove up any unwanted parts.

## 5: Setup Gruntfile.js
1. Create a file in your project folder called `Gruntfile.js` and use the example provided in this repo.

2. Install grunt in your project folder:  
`npm install grunt --save-dev`

3. Install all required packages:    
```
npm install grunt-contrib-concat --save-dev
npm install grunt-contrib-uglify --save-dev  
npm install grunt-contrib-watch --save-dev  
npm install grunt-autoprefixer --save-dev  
npm install grunt-sass --save-dev
```

## 6: Setup bower.json
 Setup bower.json by running the following command in terminal:  
```bower init```

Now you can download any bower packages required for your project. Remember that in most cases your bower packages are requirements for your poject so instead of `--save-dev` use `--save` to install them. For example:
`bower install --save bootstrap`

## 7: Install WordPress

1. Select a one word all lowercase handle or slug for this project. For example: **gigawatt**. We will use this handle or slug throughout the next few steps.

2. Download the latest copy of [WordPress CMS](https://wordpress.org/) from the wordpress.org website. Then unzip it inside the *builds* folder. Rename the *wordpress* folder to *development* effectively replacing the empty *development* folder we created earlier.

3. Now using MySQL CLI or phpmyadmin create a new empty database and name it the same as your handle/slug for the poject.

## 8: Underscores Starter Theme
1. Go to [Underscores.me](https://underscores.me/) and select *Advanced Options*.

 - **Theme Name:** Use an appropriate theme name.
 - **Theme Slug:** Use the project slug/handle we created in the Install WordPress step. :exclamation: 
 - **Author:** The Gigawatt Group
 - **Author URI:** http://gigawattgroup.com
 - **Description:** 
 - **_sassify!** :ballot_box_with_check:

2. Download and unzip underscores inside the themes directory of the wordpress install you created.

3. Inside the new Underscores theme move the `sass` folder and merge with the `sass` folder inside `components`.

4. Create the following empty files with their folders inside your Underscores theme folder:
 ```
- js/main.js
- js/main.min.js
- css/main.css
- css/main.min.css
 ```
5. Within the style.css file remove all css code below the opening comments and replace with:

 ```css
@import "css/main.css";
 ```
 
 And for production replace it with:
 
  ```css
@import "css/main.min.css";
 ```
