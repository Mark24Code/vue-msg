# vue-msg

> A Vue.js project

## 兄弟组件通信，vuex版

兄弟组件的通信在于,有一个机制能够保证监视/收听到对方的变化

A组件，触发Vuex的store.state.count 变化

B组件，computed中，一个属性依赖 store.state.count

B组件，使用watch监视，computed变量

坑：

1. 当 store.state.count是单一变量时，watch可以在直接触发
    【data.xx=state.count 只会载入一次】
2. 当 store.state.count是一个对象时，watch对应的，必须写成 deep模式 【data.xx=state.count 只会随着count变化而变化】


## Build Setup

``` bash
# install dependencies
npm install

# serve with hot reload at localhost:8080
npm run dev

# build for production with minification
npm run build
```

For detailed explanation on how things work, checkout the [guide](http://vuejs-templates.github.io/webpack/) and [docs for vue-loader](http://vuejs.github.io/vue-loader).
