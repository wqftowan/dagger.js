# dagger.js

**dagger.js** is a lightweight, zero-boilerplate, pure runtime front-end framework built for developers who value simplicity and performance. It brings a pure HTML + JavaScript development experience with no virtual DOM, no compilation step, and no complex abstractions — just clean, declarative UI.

---

## ✨ Features

- ⚡ **Zero Learning Curve**: Use plain HTML and native JavaScript — no JSX, no DSLs, no build tools required.
- ⚡ **Zero API**: dagger.js works in pure declarative mode, modules and directives provide everything you need to build your application.
- ⚡ **Reactive by Nature**: Automatic UI updates when your data changes — no manual DOM updates.
- ⚡ **Built-in Routing**: Simple, declarative routing system with no third-party dependency.
- ⚡ **Modular by Design**: Clear separation of logic and template, with automatic scoped data.
- ⚡ **Tiny & Fast**: Core runtime is just a few KB, with near-native performance.
- ⚡ **Web Native**: Fully compatible with Web Components (such as ***https://shoelace.style/***) and modern browser APIs.

---

## ✨ Installation

#### Simply insert the following script tag (CDN) insides the head section of the entry html page of your application to setup dagger.js:  
```
<script type="module" crossorigin="anonymous" src="https://cdn.jsdelivr.net/npm/@peakman/dagger.js@0.9.21/dagger.js" defer></script>
```
#### Or install dagger.js via npm:
```
npm install @peakman/dagger.js
```

---

## ✨ Directive Reference

dagger.js provides a set of pre-defined directives to declaratively render UI elements and bind data to them:

| Directive    | Description                             |
| ------------ | --------------------------------------- |
| `*checked`   | Dynamically toggle the checked state    |
| `*class`     | Dynamically toggle class names          |
| `*focus`     | Set focus on element when true          |
| `*text`      | Render plain text                       |
| `*html`      | Render raw HTML                         |
| `*each`      | Loop through an array                   |
| `*exist`     | Conditional rendering                   |
| `*value`     | Two-way binding for input elements      |
| `*selected`  | Dynamically toggle the selected state   |
| `*style`     | Dynamically bind style values           |
| `*watch`     | Run expression when dependencies change |
| `+eventName` | Event binding, e.g., `+click`, `+keyup` |
| `+load`      | Run before the element is created       |
| `+loaded`    | Run after the element is mounted        |
| `+unload`    | Run before the element is removed       |
| `+unloaded`  | Run after the element is removed        |
| `+sentry`    | Router guards                           |
| `@raw`       | Render raw HTML content without parsing |
| `@directive` | Dynamically adding directives           |

📘 [See full directive documentation →](https://daggerjs.org/#/directive/introduction)

---

## ✨ Module Configuration

dagger.js provides a simple and intuitive way to configure reusable modules for your application:

```
<script type="dagger/modules">
    {
        "view_module": "#view",
        "script_module": "#script",
        "style_module": "#style"
        ...
    }
</script>
```

📘 [See full module documentation →](https://daggerjs.org/#/module/introduction)

---

## ✨ Router Configuration

Router is a built-in feature of dagger.js that allows you to easily define routes and handle navigation between them:

```
<script type="dagger/routers">
    {
        "mode": "hash",
        "prefix": "",
        "default": "/",
        "routing": {
            "path": "",
            "tailable": true,
            "constants": {
                "title": "root title",
                "template": "view1"
            },
            "variables": {
                number: 0
            },
            "modules": ["script", "view1"],
            "children": [{
                "path": "parent1",
                "tailable": true,
                "constants": {
                "title": "parent1 title",
                "template": "view2"
                },
                "modules": "view2"
            }]
        }
        ...
    }
</script>
```

📘 [See full router documentation →](https://daggerjs.org/#/router/introduction)

---

## ✨ Demos

#### [CSS Mechanical Keyboard](https://codepen.io/dagger8224/pen/bGKPNwN)
https://github.com/user-attachments/assets/caac5818-d153-4630-a75a-d4fec72b5b94

#### [3D Tic Tac Toe](https://codepen.io/dagger8224/pen/RwMedQx)
https://github.com/user-attachments/assets/6df0fc1d-9b8e-48e0-b2c4-7c7e403ae3bc

#### [Tesla](https://codepen.io/dagger8224/pen/RwMGvPv?editors=1010)
https://github.com/user-attachments/assets/2d976e5a-5cee-4ca9-8495-764aaf4c5f85

#### [Cards](https://codepen.io/dagger8224/pen/zYWGGOY?editors=1100)
https://github.com/user-attachments/assets/a4e932af-df7a-4897-a276-88f058c80da4

#### [3D Carousel](https://codepen.io/dagger8224/pen/JjLRbmz)
https://github.com/user-attachments/assets/da23a67a-13af-45cb-97b9-9dbce2a39bf3

#### [screensaver](https://codepen.io/dagger8224/pen/rNdOBmB?editors=1010)
https://github.com/user-attachments/assets/8789d6cd-e15e-4f5f-83b3-fb4270c2363a

#### [Circular Progress Bar](https://codepen.io/dagger8224/pen/dympJXz?editors=1010)
https://github.com/user-attachments/assets/bcf78fdb-5a18-4736-8b93-88c44ac12c8b

#### [Color Picker](https://codepen.io/dagger8224/pen/vYRmGJp?editors=1010)
https://github.com/user-attachments/assets/3d1af18e-24ed-4081-88cf-339719a5f4c1

#### [Text Animation](https://codepen.io/dagger8224/pen/JjLXppg)
https://github.com/user-attachments/assets/f4e1e6b7-5744-4da5-b589-310720193d8a

And more [demos](https://codepen.io/collection/yyLOGj) on how to work with [Shoelace components](https://shoelace.style/components/).

---

## ✨ Contributing

We welcome all contributions! You can help by:

- Reporting bugs and issues

- Submitting pull requests for features or documentation

- Writing tutorials or sharing your use cases

- Spreading the word on social media

---

## ✨ Support Us

If you like dagger.js, you may:

- Star us on GitHub

- Share your projects and demos

- Join the discussions or rise issues

---

## ✨ Resources

- Official Site: https://daggerjs.org  
- Example Projects: https://codepen.io/dagger8224/pens  
- GitHub: https://github.com/wqftowan/dagger.js  
- NPM: https://www.npmjs.com/package/@peakman/dagger.js  

---

## ✨ License

[MIT](https://opensource.org/license/MIT)



