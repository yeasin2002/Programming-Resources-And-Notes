#### initialize npm empty file

```
npm init -y
```

### Install postcss

```
npm install -D  postcss  postcss-cli autoprefixer cssnano cssnano-preset-advanced
```

### use this **postcss.config.json** file

```
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

```
"build": "postcss ./src/style.pcss  -o ./public/style.css -w"
```

### Write This code in workspace setting.json

```
// postcss

"postcss.validate": false,
"emmet.includeLanguages": {
"postcss": "css",
}
```

---

## More Info:

- [Official Doc](https://postcss.org/)

- [Official Github Repo](https://github.com/postcss/postcss)

- [My Github ](https://github.com/Mdkawsarislam2002/tailwindcss-installations)

- [Postcss-Cli github repo ](https://github.com/postcss/postcss-cli)

### Some PostCSS plugging

- [cssNano](https://cssnano.co/)
- [SASS Like markup](https://github.com/csstools/precss)
- [Purgecss](https://purgecss.com/getting-started.html)
- [cssNext](https://cssnext.github.io/)
- [Stylelint github](https://github.com/stylelint/stylelint)
- [stylelint Official doc](https://stylelint.io/)
- [autoprefixer Official github rep ](https://github.com/postcss/autoprefixer)
