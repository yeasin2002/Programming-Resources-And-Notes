# Tailwindcss install Stap by Stap by postCSS 
## install process

##### initialize npm empty file

```
npm init -y
```

##### install tailwindcss by postcss with auto prefixed

```
npm install -D tailwindcss postcss autoprefixer cssnano cssnano-preset-advanced
```


##### create Tailwindcss config file

```
npx tailwindcss init
```

##### create postcss config file 
```
npx tailwindcss init -p
```



###After creating postcss.config.json file add {$this} code in there

```js
/** @type {import('tailwindcss').Config} */
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
    cssnano: {
      preset: "advanced",
    },
  },
};

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
--- 

## More: 

####  Learning recources 
[Official Doc](https://tailwindcss.com/docs/installation) - Learn With Sumit  (Bangla)

[Tailwind CSS Bangla Tutorial Series](https://youtube.com/playlist?list=PLHiZ4m8vCp9P23SqlHL0QAqiwS_oCofV2)
[Tailwind Lab - Official Tailwindcss You Tube Channel ](https://www.youtube.com/c/TailwindLabs)

#### 💙  Official resource

- 💙 [Website](https://tailwindcss.com) - Official Tailwind CSS website.
- 💙 [Repository](https://github.com/tailwindcss/tailwindcss) - Official Tailwind CSS repository.
- 💙 [Discussions](https://github.com/tailwindcss/tailwindcss/discussions) - Official place to connect with other community members about Tailwind.
- 💙 [Tailwind UI](https://tailwindui.com) - Component library made with Tailwind CSS.
- 💙 [Headless UI](https://github.com/tailwindlabs/headlessui) - Completely unstyled, fully accessible UI components.
- 💙 [Heroicons](https://heroicons.com/) - Beautiful, hand-crafted SVG icons.
- 💙 [Play](https://play.tailwindcss.com/) - Advanced online playground for Tailwind CSS.
- 💙 [Just-in-time](https://github.com/tailwindlabs/tailwindcss-jit) - Just-in-time compiler for Tailwind CSS.
- [Tailwind Weekly](https://tailwindweekly.com/) - Weekly newsletter about all things Tailwind CSS.
- [Built With Tailwind](https://builtwithtailwind.com/) - Community-driven collection of awesome websites built with Tailwind CSS.

## IDE Extensions

 💙 Official resource

- 💙 [IntelliSense for Code](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss) - IntelliSense extension for Visual Studio Code.
- [Styled Snippets for Code](https://marketplace.visualstudio.com/items?itemName=muhajirframe.tailwind-styled-snippets) - Snippet extension for Visual Studio Code.
- [Headwind for Code](https://github.com/heybourn/headwind) - Class sorter extension for Visual Studio Code.
- [Shades for Code](https://github.com/bourhaouta/vscode-tailwindshades) - Color palette generator extension for Visual Studio Code.
- [IntelliSense for Neovim](https://github.com/iamcco/coc-tailwindcss) - IntelliSense extension for Neovim.
- [Tailwind CSS Explorer for Code](https://marketplace.visualstudio.com/items?itemName=PeterMekhaeil.vscode-tailwindcss-explorer) - Explore the classes available in your project's Tailwind CSS setup.
- [Tailwind CSS Highlight](https://marketplace.visualstudio.com/items?itemName=ellreka.tailwindcss-highlight) - Highlight utilities extension for Visual Studio Code.

## Plugins

**Legend**: 💙 Official plugin · 🎨 Theming · 💼 Utilities · 🧬 Variants · 🧩 Components · 🛑 Deprecated

- 💙🧩 [Typography](https://github.com/tailwindlabs/tailwindcss-typography) - Adds a `prose` class for beautiful typographic defaults.
- 💙💼 [Aspect Ratio](https://github.com/tailwindlabs/tailwindcss-aspect-ratio) - Adds composable aspect ratio utilities.
- 💙💼 [Line Clamp](https://github.com/tailwindlabs/tailwindcss-line-clamp) - Provides utilities for visually truncating text after a fixed number of lines.
- 💙 [Forms](https://github.com/tailwindlabs/tailwindcss-forms) - Adds better default styles to form elements.
- 🎨🧬 [Theming](https://github.com/innocenzi/tailwindcss-theming) - Theming using CSS variables, with dark mode support.
- 🎨🧬 [Theme Variants](https://github.com/JakeNavith/tailwindcss-theme-variants) - Adds theme variants based on media queries and/or CSS selectors.
- 🎨🧬 [Multi Theme](https://github.com/estevanmaito/tailwindcss-multi-theme) - Adds theme variants based on a single `theme` property.
- 🎨🧬 [Theme Swapper](https://github.com/crswll/tailwindcss-theme-swapper) - Theming using CSS variables, with media queries support.
- 🎨🧬 [Themeable](https://github.com/upupming/tailwindcss-themeable) - Adds multiple themes support for Tailwind CSS.
- 🎨🧬 [Themer](https://github.com/RyanClementsHax/tailwindcss-themer) - Adds theming support for Tailwind CSS with CSS variables and variants.
- 💼🧬 [Radix](https://github.com/ecklf/tailwindcss-radix) - Adds utilities and variants for styling Radix UI state.
- 💼 [Custom Native](https://github.com/SirNavith/tailwindcss-custom-native) - Leverages Tailwind CSS's configuration to allow the creation of utilities.
- 💼 [Image Rendering](https://github.com/hacknug/tailwindcss-image-rendering) - Adds `image-rendering` utilities.
- 💼 [Elevation](https://github.com/jonaskay/tailwindcss-elevation) - Adds [Material UI `elevation`](https://material.io/design/environment/elevation.html) utilities.
- 💼 [Writing Mode](https://github.com/magicspon/tailwindcss-writing-mode) - Adds `writing-mode` utilities.
- 💼 [Hyphens](https://github.com/philippbosch/tailwindcss-hyphens) - Adds `hyphens` utilities.
- 💼 [Border Gradients](https://github.com/cossssmin/tailwindcss-border-gradients) - Adds `border-image` gradient utilities.
- 💼 [RFS](https://github.com/aerni/tailwindcss-rfs) - Adds [`RFS`](https://github.com/twbs/rfs) utilities.
- 💼 [List Reset](https://github.com/opdavies/tailwindcss-list-reset) - Adds back the `list-reset` class that was removed prior to Tailwind CSS 1.0.
- 💼 [Fluid](https://github.com/bradlc/tailwindcss-fluid) - Adds fluid sizing utilities.
- 💼 [Typography](https://github.com/benface/tailwindcss-typography) - Adds typography utilities.
- 💼 [Triangle After](https://github.com/chrisrowe/tailwindcss-triangle-after) - Adds CSS triangles utilities.
- 💼 [Scrims](https://github.com/brettgullan/tailwindcss-scrims) - Adds scrims utilities.
- 💼 [Truncate Multiline](https://github.com/jhta/tailwindcss-truncate-multiline) - Adds utilities to truncate multi-line text elements.
- 💼 [CSS Logical Properties](https://github.com/omarkhatibco/tailwind-css-logical-properties) - Generate utilities for CSS Logical Properties.
- 💼 [Tooltip Arrows After](https://github.com/gvital3230/tailwindcss-tooltip-arrow-after) - Adds CSS utilities for tooltip arrows with configurable border and background.
- 💼 [Bidirectional](https://github.com/20lives/tailwindcss-rtl) - Adds utilities for creating multilingual bidirectional layouts.
- 💼 [Bidirectional](https://github.com/yassinebridi/tailwind-direction) - Replace the core utilities to be bi-direction compatible.
- 💼 [Background SVG](https://github.com/AndersNielsen85/tailwindcss-bg-svg) - Inject SVGs as background images with color variants.
- 💼 [Background Unsplash](https://github.com/shorwood/tailwindcss-unsplash) - Apply [unsplash.com](https://unsplash.com) images as background.
- 💼 [Brand Colors](https://github.com/praveenjuge/tailwindcss-brand-colors) - Adds various brand colors for background, border and text.
- 💼 [Bootstrap Grid](https://github.com/karolis-sh/tailwind-bootstrap-grid) - Generates Bootstrap's style flexbox grid system.
- 💼 [Leading Trim](https://github.com/stormwarning/tailwindcss-capsize) - Adds utilities to trim text whitespace, using [Capsize](https://github.com/seek-oss/capsize).
- 💼 [Scrollbar Hide](https://github.com/reslear/tailwind-scrollbar-hide) - Adds `scrollbar-hide` class for visual hide scrollbar.
- 💼 [Downwind CSS Easings](https://github.com/downwindcss/easings) - Extends `transition-timing-function` utilities.
- 💼 [Content Placeholder](https://github.com/javisperez/tailwindcontentplaceholder) - Adds utilities for content placeholder images.
- 💼 [No Scrollbar](https://github.com/redwebcreation/tailwindcss-no-scrollbar) - Exposes `scrollbar-none` to visually hide a scrollbar.
- 💼 [Fluid Type](https://github.com/davidhellmann/tailwindcss-fluid-type) - Adds fluid type (`font-size`) utilities.
- 💼 [Grid Areas](https://github.com/SavvyWombat/tailwindcss-grid-areas) - Adds `grid-areas` and `grid-area` utilities.
- 🧬 [Touch](https://github.com/SteadfastCollective/tailwindcss-touch) - Adds `touch` variants.
- 🧬 [Localized](https://github.com/hdodov/tailwindcss-localized) - Adds variants based on the HTML `lang` attribute, to use utilities only with certain languages.
- 🧬 [Padded Radius](https://github.com/locksten/tailwindcss-padded-radius) - Adds variants for matching nested border radii.
- 🧬 [Fluid](https://github.com/soberwp/tailwindcss-fl) - Generates `fl:` variants.
- 🧬 [Marker](https://github.com/RadishIO/tailwindcss-marker) - Provides utilities for styling lists and `<summary>` markers.
- 🧬 [Pseudo selectors](https://github.com/Microwawe/tailwindcss-pseudo-selectors) - Adds variants for the pseudo-classes and pseudo-elements that Tailwind CSS doesn't have by default.
- 🧬 [Container Queries](https://github.com/dgknca/tailwindcss-container-query) - Adds CSS Container Query variants.
- 🧬 [FormKit](https://github.com/formkit/formkit/tree/master/packages/tailwindcss) - Adds variants for input and form states for FormKit.
- 🧩 [Debug Screens](https://github.com/jorenvanhee/tailwindcss-debug-screens) - Adds a component that shows the currently active screen (responsive breakpoint).
- 🧩 [Heropatterns](https://github.com/AndreaMinato/tailwind-heropatterns) - Adds [Hero Patterns](https://www.heropatterns.com) components.
- 🧩 [Responsive Embed](https://github.com/drdogbot7/tailwindcss-responsive-embed) - Adds a `responsive-embed` component.
- 🧩 [Bootstrap Tables](https://github.com/drehimself/tailwindcss-tables) - Adds table components based on Bootstrap's tables.
- 🧩 [Card](https://github.com/NathanHeffley/tailwindcss-card) - Adds card components.
- 🧩 [Skip link](https://github.com/opdavies/tailwindcss-skip-link) - Adds a _Skip to main content_ accessible component.
- 🧩 [Colors to CSS Variables](https://github.com/n1kk/tailwind-color-vars) - Exports color configuration to CSS Custom Properties.
- 🧩 [CSS Variables](https://github.com/omarkhatibco/tailwind-css-variables) - Exports configuration to CSS Custom Properties.
- 🧩 [CSS Variables](https://github.com/mertasan/tailwindcss-variables) - Exports custom CSS variables (Dark Mode supported).
- 🧩 [Perspective](https://github.com/Kamona-WD/tailwindcss-perspective) - Adds `perspective` utilities.

> 🛑 - _The plugins below offer functionalities that are now fully or partially implemented in Tailwind CSS._

- 🛑💼 [Caret Color](https://github.com/GraxMonzo/tailwind-caret-color) - Adds `caret` color utilities.
- 🛑💼 [Caret Color](https://github.com/naoray/tailwind-caret-color) - Adds `caret` color utilities.
- 🛑💼 [benface's gradients](https://github.com/benface/tailwindcss-gradients) - Adds gradient utilities.
- 🛑💼 [lorisleiva's gradients](https://github.com/lorisleiva/tailwindcss-plugins/tree/master/gradients) - Adds background gradient utilities.
- 🛑💼 [Visually Hidden](https://github.com/webdna/tailwindcss-visuallyhidden) - Adds screen reader utilities.
- 🛑💼 [Object Fit](https://github.com/hendrikeng/tailwindcss-object-fit) - Adds `object-fit` utilities.
- 🛑💼 [Object Position](https://github.com/hacknug/tailwindcss-object-position) - Adds `object-position` utilities.
- 🛑💼 [Accessibility](https://github.com/jack-pallot/tailwindcss-accessibility) - Adds screen reader utilities.
- 🛑💼 [Layout](https://github.com/benface/tailwindcss-layout) - Adds some layout utilities.
- 🛑💼 [Grid](https://github.com/chrisrowe/tailwindcss-grid) - Adds CSS grids utilities.
- 🛑💼 [Transforms](https://github.com/benface/tailwindcss-transforms) - Adds `transform` utilities.
- 🛑💼 [benface's transitions](https://github.com/benface/tailwindcss-transitions) - Adds configurable transition utilities, with or without CSS variables.
- 🛑💼 [webdna's transitions](https://github.com/webdna/tailwindcss-transition) - Adds configurable transition utilities.
- 🛑💼 [glhd's transitions](https://github.com/glhd/tailwindcss-plugins) - Adds basic transition utilities.
- 🛑💼 [Cursor Extended](https://github.com/hacknug/tailwindcss-cursor-extended) - Extends `cursor` utilities.
- 🛑💼 [Font Variant Numeric](https://github.com/philippbosch/tailwindcss-font-variant-numeric) - Adds `font-variant-numeric` utilities.
- 🛑💼 [Filters](https://github.com/benface/tailwindcss-filters) - Adds `filter` utilities.
- 🛑💼 [CSS Filters](https://github.com/Larsklopstra/tailwindcss-css-filters) - Adds `filter` and `backdrop-filter` utilities with defaults.
- 🛑💼 [Blend Mode](https://github.com/hacknug/tailwindcss-blend-mode) - Adds `blend-mode` utilities.
- 🛑💼 [Colorize](https://github.com/philippbosch/tailwindcss-colorize) - Adds `filter` utilities.
- 🛑💼 [Scroll Snap](https://github.com/innocenzi/tailwindcss-scroll-snap) - Adds `scroll-snap` utilities.
- 🛑💼 [Scroll Behavior](https://github.com/lukewarlow/tailwind-scroll-behavior) - Adds `scroll-smooth` and `scroll-auto` classes to control smooth scrolling.
- 🛑💼 [Accent Color](https://github.com/lukewarlow/tailwind-accent-color) - Adds accent color utilities.
- 🛑💼 [Text Indent](https://github.com/hacknug/tailwindcss-text-indent) - Adds `text-indent` utilities.
- 🛑💼 [Text Decoration Color](https://github.com/ahmadawais/tailwind-text-decoration-color) - Adds `text-decoration-color` utilities.
- 🛑💼 [Downwind CSS Text Decoration](https://github.com/downwindcss/text-decoration) - Adds composable `text-decoration` utilities.
- 🛑💼 [Capitalize first letter](https://github.com/riderx/capitalize-first-tailwind) - Adds `capitalize-first` utilities.
- 🛑💼 [Aspect Ratio](https://github.com/webdna/tailwindcss-aspect-ratio) - Adds `aspect-ratio` utilities.
- 🛑💼 [Shadow Outline Colors](https://github.com/octoper/tailwindcss-shadow-outline-colors) - Adds `box-shadow` utilities based on configured colors.
- 🛑💼 [Alpha](https://github.com/bradlc/tailwindcss-alpha) - Adds alpha color variant utilities.
- 🛑🧬 [Direction](https://github.com/RonMelkhior/tailwindcss-dir) - Adds `RTL` and `LTR` variants.
- 🛑🧬 [Important](https://github.com/chasegiunta/tailwindcss-important) - Adds an `important` variant.
- 🛑🧬🎨 [Prefers Dark Mode](https://github.com/javifm86/tailwindcss-prefers-dark-mode) - Adds variants based on the `prefers-color-scheme` media query.
- 🛑🧬🎨 [Dark Mode](https://github.com/danestves/tailwindcss-darkmode) - Adds `dark` variants based on CSS classes.
- 🛑🧬🎨 [Dark Mode](https://github.com/ChanceArthur/tailwindcss-dark-mode) - Adds `dark` variants based on the `prefers-color-scheme` media query.
- 🛑🧬 [CSS Alpha Colors](https://github.com/soueuls/tailwind-color-alpha) - Adds opacity variants to existing colors.
- 🛑🧬 [Pseudo](https://github.com/Log1x/tailwindcss-pseudo) - Adds custom variants to Tailwind CSS's configuration.
- 🛑🧩 [Spinner](https://github.com/aniftyco/tailwindcss-spinner) - Adds a spinner component.
- 🛑🧩 [Spaced Items](https://github.com/n1kk/tailwindcss-spaced-items) - Adds `spaced` components that add fixed margins to all container items.
- 🛑🧩💙 [Custom Forms](https://github.com/tailwindlabs/tailwindcss-custom-forms) - Adds better default styles to form elements.

## Tools

**Legend**: 🌍 Accessible online · 🔼 Conversion or upgrade tool · 🔧 Generator · 🅰 Typing/enforcement · 💼 Plugins/Tools/Extensions for external services · 🎨 Color-related · 🚀 Framework

- 🎨🌍🔧 [Tailwind Color Shades](https://javisperez.github.io/tailwindcolorshades) - Color shades generator for Tailwind CSS.
- 🎨🌍🔧 [Palette generator](https://adevade.github.io/color-scheme-generator) - Color palette generator that outputs Tailwind CSS configuration files.
- 🎨🌍🔧 [Tailwind Colors](https://tailwind-colors.meidev.co) - Color configuration generator for Tailwind CSS.
- 🎨🌍🔧 [Tailwind Color Explorer](https://stefanbuck.com/tailwind-color-theme-explorer) - Color explorer for Tailwind CSS.
- 🎨🌍🔧 [TailwindInk](https://tailwind.ink/) - AI palette generator, trained with the Tailwind CSS palette.
- 🎨🌍🔧 [Gradient Designer](https://gradient-designer.csspost.com/) - Generate gradients for Tailwind 2.0+.
- 🎨🌍🔧 [Grayscale Design](https://grayscale.design/) - A Luminance-based color palette generator.
- 🎨🌍🔧 [Hypercolor](https://hypercolor.dev/) - Collection of pre-configured Tailwind CSS gradients with directional options.
- 🎨🌍🔧 [Palettolithic](https://palettolithic.com) - Generates harmonius color palettes based on one color.
- 🎨🌍🔧 [Tailwind Gradient Generator](https://tailwindcomponents.com/gradient-generator) - Create perfect Tailwind CSS gradients with zero lines of code.
- 🎨🌍🔧 [Ui Colors](https://uicolors.app/create) - Color palette generator for Tailwind CSS.
- 🎨🌍💼 [Tailwind CSS v2 colors](https://www.figma.com/community/file/905719775911766776) - Figma library with Tailwind CSS v2 colors.
- 🎨🔧💼 [Colorkraken](https://github.com/Bouhoum/colorkraken) - Color shades generator for Tailwind CSS.
- 🎨🔧💼 [babel-plugin-tailwind-dark](https://github.com/wowlusitong/babel-plugin-tailwind-dark) - A Babel plugin to add custom dark class when compiling your code using Babel.
- 🌍🔧💼 [Twind](https://github.com/tw-in-js/twind) - Compiler functions that turn Tailwind's classes into CSS at run, serve and build time.
- 🌍🔧 [GPT-3 Tailwind CSS code generator](http://gpt-tailwind.com/) - OpenAI GPT-3 powered Tailwind CSS code generator.
- 🌍🔧 [Stitches](https://stitches.hyperyolo.com/) - Template generator with Tailwind (online).
- 🌍🔧 [tail-animista](https://tail-animista.vercel.app) - Configurable custom animation utilities generator for Tailwind CSS.
- 🌍🔧 [brands-tail-color](https://brands-tail-color.vercel.app/) - Configuration generator using various brands' colors.
- 🌍🔧 [Windframe](https://www.devwares.com/windframe/) - Tailwind CSS drag and drop builder to rapidly build and prototype websites.
- 🌍 [Typography Playground](https://tailwind-typography-playground.vercel.app/) - Tool for trying different Google Fonts combinations with the Tailwind CSS Typography Plugin.
- 🌍💙 [Play](https://play.tailwindcss.com/) - Advanced online playground for Tailwind CSS.
- 🌍 [Updrafts.app](https://updrafts.app/) - Advanced online no-code drag and drop editor for Tailwind CSS.
- 🌍 [tailwind.run](https://tailwind.run) - Tailwind CSS fiddle with built-time features (online).
- 🌍 [tailzilla.app](https://tailzilla.app) - Online playground for Tailwind CSS.
- 🌍 [Flowrift](https://flowrift.com) - Beautifully designed Tailwind CSS UI blocks.
- 🔼🌍 [Tailwind Automatic Prefix Applicator](https://github.vue.tailwind-prefix.cbass.dev) - Tailwind classes' prefixer tool.
- 🔼🌍 [CSS to Tailwind CSS Converter](https://transform.tools/css-to-tailwind) - Converts CSS to Tailwind CSS by suggesting classes that best match.
- 🔼 [Tailwindo](https://github.com/awssat/tailwindo) - Bootstrap to Tailwind CSS converter.
- 🔼 [Tailupgrade](https://github.com/virkillz/tailupgrade) - Conversion tool for upgrading HTML files from Tailwind CSS v0.x to v1.0.
- 🔼 [Tailwind Shift](https://github.com/awssat/tailwind-shift) - Upgrade tool for upgrading from Tailwind CSS v0.7 to v1.0.
- 🔼 [RustyWind](https://github.com/avencera/rustywind) - CLI tool for sorting Tailwind CSS classes.
- 🔼 [Windy](https://usewindy.com) - Browser extension to convert HTML elements to Tailwind CSS.
- 🅰 [react-native-tailwindcss](https://github.com/TVke/react-native-tailwindcss) - React Native typing system.
- 🅰 [typed-tailwind](https://github.com/dvkndn/typed-tailwind) - TypeScript typings for Tailwind CSS.
- 💼 [Gatsby Plugin](https://github.com/muhajirframe/gatsby-plugin-tailwindcss) - Tailwind CSS integration for Gatsby.
- 💼 [Gridsome Plugin](https://github.com/brandonpittman/gridsome-plugin-tailwindcss) - Tailwind CSS integration for Gridsome.
- 💼 [Alfred Workflow](https://github.com/clnt/alfred-tailwindcss-docs) - Fast Tailwind CSS documentation search application.
- 💼 [ng-tailwindcss](https://github.com/tehpsalmist/ng-tailwindcss) - CLI tool for integrating Tailwind CSS into Angular-CLI projects.
- 💼 [vue-cli-plugin-tailwind](https://github.com/forsartis/vue-cli-plugin-tailwind) - Vue CLI plugin that adds Tailwind CSS to a project.
- 💼 [Tailwind CSS Figma Kit](https://github.com/ecklf/tailwindcss-figma-kit) - Figma Kit for Tailwind CSS.
- 💼 [Tailwind CSS Figma UI Design Kit](https://flowbite.com/figma/) - Figma UI Design Kit for Tailwind CSS.
- 💼 [Tailwind CSS Figma Plugin](https://github.com/ecklf/tailwindcss-figma-plugin) - Figma plugin that integrates Tailwind CSS.
- 💼 [@nuxtjs/tailwindcss](https://github.com/nuxt-community/tailwindcss-module) - Tailwind CSS module for NuxtJS with PurgeCSS and modern CSS (preset env 1).
- 💼 [preact-cli-tailwind](https://github.com/agneym/preact-cli-tailwind) - Tailwind CSS integration for Preact.
- 💼 [tailwind-classes-sorter](https://github.com/Acidic9/tailwind-classes-sorter) - NPM library which provides a utility to sort Tailwind CSS classes.
- 💼 [prettier-plugin-tailwind](https://github.com/Acidic9/prettier-plugin-tailwind) - Prettier plugin that sorts class lists.
- 💼 [tailwindcss-rails](https://github.com/rails/tailwindcss-rails) - Gem for using Tailwind CSS with Rails' asset pipeline.
- 💼🔧 [Zeplin Config & Class generator](https://extensions.zeplin.io/5ae2d20017c57fd249c9876f) - Zeplin extension that generates Tailwind configurations.
- 💼🔧 [@tailwindcssinjs/macro](https://github.com/Arthie/tailwindcssinjs) - Babel macro that transforms Tailwind CSS classes into objects for CSS-in-JS libraries.
- 💼🔧 [twin.macro](https://github.com/ben-rogerson/twin.macro) - Use Tailwind classes within any CSS-in-JS library.
- 💼🔧 [tailwindcss-webpack-plugin](https://github.com/await-ovo/tailwindcss-webpack-plugin) - Out-of-the-box Tailwind CSS, supports "Design in Devtools" mode and visualizes Tailwind CSS configuration.
- 💼🔧 [Tailwind Config Viewer](https://github.com/rogden/tailwind-config-viewer) - Local UI tool for visualizing your Tailwind CSS configuration file.
- 💼🔧 [Laravel Form Components](https://github.com/pascalbaljetmedia/laravel-form-components) - Blade form components using Tailwind CSS Custom Forms.
- 💼 [@ngneat/tailwind](https://github.com/ngneat/tailwind) - Tailwind CSS integration for Angular.
- 💼 [Gust](https://www.getgust.com) - Drag and drop page builder for WordPress.
- 💼 [clb](https://github.com/crswll/clb) - clb (class list builder) is a utility function that builds a class list based on a [Stitches](https://stitches.dev/) like API.
- 💼🌍 [Inspect Flow](https://inspectflow.io) - The complete developer tool for Tailwind CSS.
- 💼 [twined-components](https://github.com/lowfront/twined-components) - Extended component of a styled-components that prioritizes class names for use in Tailwind CSS.
- 🔧 [re-tailwind](https://github.com/phthhieu/re-tailwind) - ReasonML utility that generates Tailwind classes.
- 🔧 [Protoship Codegen](https://protoship.io) - Code generator that creates Tailwind CSS based HTML & CSS from Sketch designs.
- 🔧 [create-tailwind-plugin](https://github.com/Landish/create-tailwind-plugin) - Plugin scaffolder for Tailwind CSS.
- 🚀 [Maizzle](https://maizzle.com/) - Framework for rapid email prototyping with Tailwind CSS.
- 🌍 [Tailwind Cheat Sheet](http://nerdcave.com/tailwind-cheat-sheet) - Tailwind CSS class names cheat sheet.
- 🌍 [Tailwind Cheat Sheet](https://github.com/LeCoupa/awesome-cheatsheets/blob/master/frontend/tailwind.css) - Tailwind CSS class names in one single file.
- 🌍 [Tailwind Cheat Sheet](https://umeshmk.github.io/Tailwindcss-cheatsheet) - Tailwind CSS class names, variants and directives cheat sheet.
- 🌍 [Tailwind Cheat Sheet](https://tailwindcomponents.com/cheatsheet) - Tailwind CSS class names in a searchable page.
- 🌍 [Tailwind Cheat Sheet](https://flowbite.com/tools/tailwind-cheat-sheet/) - Tailwind CSS utility class names in a searchable interface.

## UI Libraries, Components & Templates

**Legend**: 💙 Official resource · 📚 Library · 🧩 Components · 📁 Templates

- 💙🧩 [Tailwind UI](https://tailwindui.com) - Component library made with Tailwind CSS.
- 💙📚 [Headless UI](https://github.com/tailwindlabs/headlessui) - Completely unstyled, fully accessible UI components.
- 📚 [VueTailwind](https://github.com/alfonsobries/vue-tailwind) - Vue.js UI library using Tailwind CSS.
- 📚 [Tailwind Elements](https://tailwind-elements.com/) - Huge collection of free components, mobile-friendly thanks to Bootstrap 5.
- 📚 [Vechai UI](https://www.vechaiui.com/) - High-quality accessible React components with the built-in dark mode using Tailwind CSS.
- 📚 [Flowbite](https://flowbite.com/docs/getting-started/introduction/) - Open-source component library built with Tailwind CSS.
- 📚 [a17t](https://a17t.miles.land) - Atomic design toolkit built to extend Tailwind CSS.
- 📚 [tails-ui](https://github.com/knipferrc/tails-ui) - React UI library using Tailwind CSS.
- 📚 [tails](https://github.com/thedevdojo/tails) - Hand-crafted templates and components using Tailwind CSS.
- 📚 [Svelte Headless UI](https://github.com/rgossiaux/svelte-headlessui) - Unofficial Svelte port of Headless UI.
- 📚 [Xtend UI](https://xtendui.com/) - Tailwind CSS components with advanced interactions and animations.
- 📚 [Headless UI Float](https://headlessui-float.vercel.app) - Floating UI integration for Headless UI.
- 🧩 [TailBlocks](https://mertjf.github.io/tailblocks) - 60+ different ready to use Tailwind CSS blocks.
- 🧩 [Tailwind Components](https://tailwindcomponents.com) - Community-driven Tailwind CSS component repository.
- 🧩 [Tailwind Toolbox](https://www.tailwindtoolbox.com) - Templates, components and resources.
- 🧩 [Meraki UI Components](https://merakiui.com) - Beautiful Tailwind CSS components that support RTL languages.
- 🧩 [Tailwind Cards](https://github.com/hasinhayder/tailwind-cards) - Growing collection of text/image cards.
- 🧩📁 [Tailwind Templates](https://www.tailwindtemplates.io) - Collection of templates and components.
- 🧩📁 [Treact](https://treact.owaiskhan.me) - React UI templates and components built using Tailwind CSS.
- 🧩📁 [Jakarta LTE](https://github.com/zeroblack-c/jakarta-lte) - Admin template using Tailwind CSS.
- 🧩📁 [themes.dev](https://www.themes.dev/) - Handcrafted, free and premium Tailwind CSS themes and components.
- 🧩 [Kutty](https://kutty.netlify.app) - Accessible and reusable components that are commonly used in web applications.
- 🧩 [Sail UI](https://sailui.github.io/) - Collection of basic UI components built on Tailwind CSS.
- 🧩 [jQuery Toggler](https://craigerskine.github.io/jquery-tailwind-checkbox-toggle) - Switches using jQuery and Tailwind CSS.
- 🧩 [Tailwind Kit](https://creative-tim.com/learning-lab/tailwind-starter-kit) - Framework-agnostic, Vue.js, React and Angular components.
- 🧩 [lofi ui](https://lofiui.co/) - Low-fidelity Tailwind CSS components.
- 🧩 [Gust UI](https://www.gustui.com/) - Sleek Tailwind CSS components for web applications in React and HTML.
- 🧩 [Windstrap](https://windstrap.netlify.app) - Tailwind CSS with Bootstrap JS.
- 🧩 [WickedBlocks](https://blocks.wickedtemplates.com/) - Collection of more than 120 layout blocks and components built with Tailwind CSS.
- 🧩 [Daisy UI](https://github.com/saadeghi/daisyui) - UI Components for Tailwind CSS.
- 🧩 [Kometa UI Kit](https://kitwind.io/products/kometa/components) - Free multi-purpose UI kit, built with Tailwind CSS.
- 🧩 [Mamba UI](https://mambaui.com) - Free Tailwind CSS components, sections and templates.
- 🧩 [Litepie Date picker](https://github.com/kenhyuwa/litepie-datepicker) - A date range picker component for Vue.js and Tailwind CSS.
- 🧩 [Tailwind Datepicker](https://github.com/themesberg/tailwind-datepicker) - Adds a datepicker component built with Tailwind CSS and vanilla JavaScript.
- 🧩 [Tailwind Typeahead](https://github.com/basarozcan/vue-tailwindcss-typeahead) - Typeahead/Autocomplete component built with Vue.js and Tailwind CSS.
- 🧩 [Material Tailwind](https://material-tailwind.com/) - Easy to use components library for Tailwind CSS and Material Design.
- 🧩 [Layouts for Tailwind](https://layoutsfortailwind.lalokalabs.dev/) - Layouts and UI Patterns for Tailwind CSS.
- 🧩 [HyperUI](https://hyperui.dev/) - Open source marketing and ecommerce Tailwind CSS components.
- 🧩 [Snippets](https://snippets.alexandru.so/) - Open source collection of animation snippets made for Tailwind CSS.
- 🧩 [Fancy Tailwind](https://fancytailwind.com/) - Large collection of Tailwind CSS UI components (700+).
- 🧩 [Myna UI](https://mynaui.com/) - Open source UI Components and Marketing Elements made with Tailwind CSS.
- 📁 [Vue Notus](https://www.creative-tim.com/product/vue-notus) - Open-source Tailwind CSS and Vue.js UI kit.
- 📁 [Red Pixel Themes](https://redpixelthemes.com/) - Paid, developer-friendly templates made with Tailwind CSS.
- 📁 [EasyTailwind](https://easytailwind.now.sh) - Freemium, easily customizable templates made with Tailwind CSS.
- 📁 [Windmill Dashboard](https://windmill-dashboard.vercel.app/) - Multi theme, completely accessible dashboard template.
- 📁 [Tailwind Admin](https://github.com/tailwindadmin/admin) - Administration panel template with Tailwind CSS.
- 📁 [Landing Gradients](https://landing-gradients.netlify.app/) - Landing page template using gradients (1.7+).
- 📁 [Resume](https://github.com/mohusman360/mohusman360.github.io) - Simple resume with Tailwind CSS.
- 📁 [Resume](https://github.com/Thomashighbaugh/resume) - A stylized resume template built with Tailwind CSS, featuring a nifty hero-pattern background and custom font.
- 📁 [Simple Light](https://github.com/cruip/tailwind-landing-page-template) - Free landing page template built with React & Tailwind CSS.
- 📁 [V-Dashboard](https://github.com/wobsoriano/v-dashboard) - Dashboard starter template built with Vue 3 and Tailwind CSS.
- 📁 [Petra](https://github.com/Smuice-com/Free-Nuxtjs-Tailwindcss-landing-page-template) - Free landing page template built with Nuxt.js & Tailwind CSS.
- 📁 [Tailmin](https://github.com/otezz/tailmin) - Admin dashboard built with Vue.js and Tailwind CSS.
- 📁 [OhMySMTP Templates](https://github.com/ohmysmtp/templates) - Set of Transactional HTML Email Templates, built with Maizzle
- 📁 [Material Tailwind Kit React](https://www.creative-tim.com/product/material-tailwind-kit-react) - Free Tailwind CSS and React UI kit.
- 📁 [Material Tailwind Dashboard React](https://www.creative-tim.com/product/material-tailwind-dashboard-react) - Free Tailwind CSS and React admin template.
- 📁 [Admin One Vue 3](https://github.com/justboil/admin-one-vue-tailwind) - Free Vue.js 3 Tailwind CSS admin template with Vite & Vue CLI support.
- 📁 [Cruip](https://cruip.com/) - Beautifully designed HTML, React, and Vue.js templates.


