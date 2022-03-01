# Tailwindcss install Stap by Stap by postCSS 
## install process

##### initialize npm empty file

```
npm init -y
```

##### install tailwindcss by postcss with auto prefixed

```
npm install -D tailwindcss postcss autoprefixer
```

##### create Tailwindcss config file

```
npx tailwindcss init
```

##### create postcss config file 
```
npx tailwindcss init -p
```
### use this code in **packege.json** file for _build_

#### create a public  folder  and create index.html file  and a **style.css** file 
#### then  create a src folder  and on there create a **tailwind.css** file 

#### add this in your **tailwind.css** file 
###### *(note: you can name it whatever you want and create or create all file where you want) *
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```


#### use this code on your scripts tag on your  package.json file   ( on scripts tag)
```json
    "build": " npx tailwindcss -i ./src/tailwind.css  -o ./public/style.css -w",
    "build-p": "postcss ./src/tailwind.css  -o ./public/style.css -w"
```

### Add the paths to all of your template files in your **tailwind.config.js** file.

```javaScript
module.exports = {
  content: ["./src/**/*.{html,js}"],
  // no need this from here this are for example  , just need to add this path 
  theme: {
    extend: {},
  },
  plugins: [],
};

```

#### create .vscode folder  and in there  create settings.json file , add this in that file 
###### this for tailwindCSS auto-complete and it's not going to show error 

```json
{
  "css.validate": false,
  "tailwindCSS.emmetCompletions": true
}

```

#### Run Tailwind CSS by post CSS 

```
npm run build -p 
```


# Automatic Class Sorting with Prettier
 #### install prettier Extension from VS Code Marketplace   Or using CLI command 
```
npm install --save-dev prettier-plugin-tailwind-css
```
 ```
 yarn add -D prettier-plugin-tailwind-css
 ```
----------
## Using prettier with tailwind in your workspace 
### Create a file in this name 
```
.prettierrc.json
```
## use this command to run pretteir in your project (for all file use a dot. or use your file name)
```
npx prettier --write . 
```

#### Add "removeDuplicatesClasses" in  Json file to remove duplicate class  
```
{ "removeDuplicatesClasses": true }
```

