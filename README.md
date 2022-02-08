# Tailwindcss install with JIT mode

## install process

##### initialise npm emty file

```
npm init -y
```

##### install tailwindcss by postcss with auto prefixer

```
npm install -D tailwindcss postcss autoprefixer
```

##### creat tailwincs config file

```
npx tailwindcss init
```

##### creat postcss config file 
```
npx tailwindcss init -p
```
### use this code in **packege.json** file for _build_

#### creat a public  folder  and creata index.html file  and a **style.css** file 
#### then  creat a src folder  and on there creat a **tailwind.css** file 

#### add this in your **tailwind.css** file 
###### *(note: you can name it whatever you want and creat or creat  all file where where you want)*
```css
@tailwind base;
@tailwind components;
@tailwind utilities;
```


#### use this code on  your scripts tag  on your  package.json file   ( on scripts tag)
```json
    "build": " npx tailwindcss -i ./src/tailwind.css  -o ./public/style.css -w",
    "build-p": "postcss ./src/tailwind.css  -o ./public/style.css -w"
```

### use this code in **tailwind.config.js file** for _JIT MODE_

```javaScript
module.exports = {
  mode: "jit",
  content: ["./public/**/*.html"],
  theme: {
    extend: {},
  },
  plugins: [],
};

```

#### creat .vscode folder  and in there  creat settings.json file , add this in that file 
###### this for tailwindcss auto complate and it's not gonna show error 

```json
{
  "css.validate": false,
  "tailwindCSS.emmetCompletions": true
}

```

#### Run taliwindcss by post css 

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
## Using prettier  with tailwind in your workspace 
### Create a file  in this name 
```
.prettierrc.json
```
## use this command to run pretteir in your project  ( for all file use a dot . or use your file name  )
```
npx prettier --write . 
```

#### Add "removeDuplicatesClasses" in  json file to remove duplicate  class  
```
"removeDuplicatesClasses" : true,
```
