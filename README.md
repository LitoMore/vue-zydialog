## Vue ZyDialog

A dialog component that provides customizable `alert`, `confirm` and `prompt` for your Vue.js apps.

[Checkout the DEMO](https://mogita.github.io/vue-zydialog)

### Features

- Promise based, friendly programming interface
- Global and per call config
- Sequential calls are queued automatically, while it's possible to override the priority manually
- Zero styling dependency, theming (WIP) based on CSS
- Mobile & desktop ready

### Requirement

- Vue.js 2.x

### Browser Compatibility

- Evergreen browsers
- IE >= 9

### Installation

With Yarn

```
yarn add vue-zydialog
```

Or with NPM

```
npm install vue-zydialog --save
```

### Basic Example

Import ZyDialog in your `main.js` file

```js
import ZyDialog from 'vue-zydialog'
Vue.use(ZyDialog)
```

Use it in your `vue` component

```js
...
methods: {
  sayHello () {
    this.$alert('Hello world')
    .then(() => {
      this.$alert('World confirmed')
    })
  }
}
...
```

If you prefer the `async/await` flavour, you can do this

```js
...
methods: {
  async sayHello () {
    await this.$alert('Hello world')
    this.$alert('World confirmed')
  }
}
...

...
methods: {
  async toConfirm () {
    if (await this.$confirm('Are you sure?')){
      // continue to process
    } else {
      // abort processing
    }
  }
}
...
```

### Documentation

(Docs WIP)

### License

[MIT](https://tldrlegal.com/license/mit-license)