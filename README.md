# vue-threejs

> \[WIP\] [Vue][vue] bindings for [Three.js][threejs]

> Migrated from [react-threejs](https://github.com/fritx/react-threejs)

<img width="400" src="https://github.com/fritx/react-threejs/raw/dev/debugging.jpg">

```js
import VueThreejs from 'vue-threejs'
Vue.use(VueThreejs)
```

```vue
<template>
  <renderer :size="{ w: 600, h: 400 }">
    <scene>
      <camera :position="{ z: 15 }"></camera>
      <object3d :obj="mesh" :position="{ y: -200 }"></object3d>
    </scene>
  </renderer>
</template>
```

**Roadmap**

- [ ] Basic components
  - [x] light
  - [ ] controls
- [ ] Watch for props change
  - [x] position/rotation
  - [ ] obj/more
- [ ] Better animation mechanism
  - [x] animation-component
  - [x] animation-component-plain
  - [x] animation-mixin
  - [ ] animation queue/container

**Study Notes**

- [Vue2 migration commits of vue-threejs](https://github.com/fritx/vue-threejs/commits/vue2)
  - `cannot use <slot> as root element`
  - `lifecycle ready => mounted`
  - `template or render function not defined`
  - `avoid mutating a prop directly`
  - `this.$dispatch is not a function`
- [v-ref is not working with <template> element](https://github.com/vuejs/vue/issues/681#issuecomment-75802646)
- [Can I use a compoent inherit other compoent?](https://github.com/vuejs/Discussion/issues/354#issuecomment-133019536)

[react-threejs]: https://github.com/fritx/react-threejs
[threejs]: https://github.com/mrdoob/three.js
[vue]: https://github.com/vuejs/vue
