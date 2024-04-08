How to setup Professional Project ? 

1> npm init
npm init is a command used in Node.js projects to initialize a new Node.js project and create a package.json file. This file serves as a manifest for the project, containing metadata such as the project name, version, description, entry point, dependencies, and other important information.

2> add readme.md
Project overview -> Installations instructions -> Usage -> Configuration -> Examples -> Contributing -> Licence

3> Go to package.json  && add "type" : "module"
This is used to choose a method to import a module in your project
common : require ()
module : import {} from ""

4> Connection with github
git init
git add.
git commit -m ""
git branch -M main
Create a empty new repo in github
git remote add origin url => (url of new github repo)
Create a new token from Developer settings
git remote set-url origin https://<token>@url => (github.com/project url)
git push -u origin main

5> New public folder
add public folder
In public, add temp folder (: to add images there)
At this time temp is empty so somehow git will not keep track of it,
So add .gitkeep file in it.

6> Make src folder
In src folder, add index.js -> constants.js -> app.js

7> Install nodemon
It basically restarts the server when you save the code.
It is a developer dependancy. 
So we dont want to pass it to production code.
Thats why install it using
npm install -D nodemon ( -D : developer dependancy)

8> Go in package.json & in scripts add "dev" : "nodemon index.js"

9> Add some folders in src folder
controllers -> db -> middlewares -> models -> routes -> utils

10> Install prettier
To avoid conflicts at the time of deployment.
npm i -D prettier
Then add some files

11> add .prettierrc
{
    "singleQuote": false,
    "bracketSpacing": true,
    "tabWidth": 2,
    "trailingComma": "es5",
    "semi": true
}

12> add .prettierignore
Do not use prettier in these files
*.env
.env
.env.*

/node_modules
/.vscode
./dist