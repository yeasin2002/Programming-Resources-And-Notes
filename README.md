#### initialize npm empty file

```
npm init -y
```

### Install postcss

```
npm install -D  postcss  postcss-cli autoprefixer cssnano cssnano-preset-advanced
```

### use this **postcss.config.js** file

```js 
module.exports = {
  plugins: {
    autoprefixer: {},
    cssnano: {
      preset: "advanced",
    },
  },
};

```

### use this in **package.json** on **script** tag
# you can use deferent file path as you want But make sure to writw correct path here 

```json
"build": "postcss ./src/style.pcss  -o ./public/style.css -w"
```

### Write This code in workspace setting.json

```json

"postcss.validate": false,
"emmet.includeLanguages": {
"postcss": "css",
}
```

---


### Now Open Terminals And  Write This command And Hit Enter 
```
npm run  build 
```
 
## More Info:

- [Official Doc](https://postcss.org/)

- [Official Github repository](https://github.com/postcss/postcss)

- [My Github ](https://github.com/Mdkawsarislam2002/tailwindcss-installations)

- [Postcss-Cli github repository ](https://github.com/postcss/postcss-cli)

### Some PostCSS plugging

- [cssNano](https://cssnano.co/)
- [SASS Like markup](https://github.com/csstools/precss)
- [Purgecss](https://purgecss.com/getting-started.html)
- [cssNext](https://cssnext.github.io/)
- [Stylelint github](https://github.com/stylelint/stylelint)
- [stylelint Official doc](https://stylelint.io/)
- [autoprefixer Official github repository  ](https://github.com/postcss/autoprefixer)
- [Find All Plunging Fore Here ](https://www.postcss.parts/)
- [Import plugging ](https://github.com/postcss/postcss-import)
- [SASS Like Import ](https://github.com/csstools/postcss-partial-import)
- [media min-max](https://github.com/postcss/postcss-media-minmax)
- [PostCSS Nesting](https://github.com/csstools/postcss-plugins/tree/main/plugins/postcss-nesting)
 
### Tutorials 
- [PostCSS Crush Course ](https://youtu.be/RuLrIJJzt60)
- [ PostCSS  in 100 second ](https://youtu.be/WhCXiEwdU1A)
- [ Bacic Overview of PostCSS](https://youtu.be/WhCXiEwdU1A) 
- [ PostCSS Playlists With Gulp](https://youtube.com/playlist?list=PLLnpHn493BHFvjZzyYrQP0RTsG-Al7j9m)
