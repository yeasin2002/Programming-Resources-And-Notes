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

##### creat postcss file

```
npm run build -p
```

### use this code in **packege.json** file for _build_

###### use your own file

```
"scripts": {
    "build": "tailwindcss -i ./src/tailwind.css  -o ./public/style.css -w",
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

#### Run taliwindcss

```
npm run build
```
