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

###### use your own file

```
"scripts": {
    "build": " npx tailwindcss -i ./src/tailwind.css  -o ./public/style.css -w",
    "build-p": "postcss ./src/tailwind.css  -o ./public/style.css -w"
  },
```

### use this code in **tailwind.config.js file** for _JIT MODE_

```
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

```
{
  "css.validate": false,
  "tailwindCSS.emmetCompletions": true
}

```

#### Run taliwindcss by post css 

```
npm run build -p 
```
