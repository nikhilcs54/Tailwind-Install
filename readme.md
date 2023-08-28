Step 1: Create a project folder

Create a folder and write the desired name on that folder. Inside that folder, create an HTML file and add boilerplate code(use ! then press enter).

Step 2: Install npm necessary files

Once you created a folder with an HTML file, then open the terminal on the project’s root directory and type the below command into the terminal. This command will simply generate an empty npm project and Here, -y stands for yes. A file named package.json was created. (This step can be skipped but I prefer it to use)

npm init -y
Step 3: Installing tailwind CSS along with vite.js

Run the following command on the terminal to install all the tailwind dependencies through vite. This command will create a node_modules folder and package-lock.json file.

npm install -D tailwindcss postcss autoprefixer vite
Step 4: Create Tailwind config file

The below command will generate 2 config files named postcss.config.js and tailwind.config.js.

npx tailwindcss init -p
postcss.config.js 

Javascript
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
}
tailwind.config.js 

Javascript
/** @type {import('tailwindcss').Config} */
 
module.exports = {
  content: [],
  theme: {
    extend: {},
  },
  plugins: [],
}
Step 5: Adding Tailwind directives

Now, create a style.css file, and inside that file, add the layer directives of tailwind CSS. Once all the layer directives will be added in style.css, now, link the style.css file into your HTML file using the <link> tag.

@tailwind base;
@tailwind components;
@tailwind utilities;
Step 6: Updates in package.json

We have created a package.json file (in step 2). This file contains important metadata about your project and records your dependencies. 

“scripts”: {
   “test”: “echo \”Error: no test specified\” && exit 1″
 },

Change the above lines of code with the lines below and don’t forget to add a comma at the end.

“scripts”: {
   “start”: “vite”
 },

Step 7: Configure template paths

We need to update the content in the tailwind.config.js file so that it will apply tailwind-CSS in all the files.

Javascript
// Older version of tailwind.config.js file
 
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: [],
  theme: {
    extend: {},
  },
  plugins: [],
}
Line to update

content: ["*"],
After updating the tailwind.config.js file:

Javascript
// After update
 
/** @type {import('tailwindcss').Config} */
module.exports = {
  content: ["*"],
  theme: {
    extend: {},
  },
  plugins: [],
}
Step 8: Check project structure

Check the project structure and all the necessary files. 


 

Step 9: Run the application

To run the application use the command npm run start into the terminal.

npm run start
The above line of code will generate a localhost server, & follow the server link to open the application on the web browser.