---
title: 'vue form'
date: '17:34 06/27/2017'
taxonomy:
    category:
        - blog
    tag:
        - photography
        - architecture
hero_classes: 'text-dark title-h1h2 overlay-light hero-large parallax'
blog_url: /blog
subtitle: 'form'

header_image_alt_text: Modern building
---


## html

```html
<div id="app">
  <main-form :data="data"></main-form>
</div>
```

## .vue
```js
Vue.component("main-form", {
  template: `
<div>
  <tabs>
    <tab>
      <part1-of-form :data="data"/>
    </tab>
    <tab>
      <part2-of-form :data="data"/>
    </tab>
  </tabs>
  <button @click='onSave'>Save</button>
  <div>{{ savedData }}</div>
</div>
`,
  data: function() {
    return {
      savedData: null
    };
  },
  props: {
    data: Object
  },
  methods: {
    onSave: function() {
      this.savedData = { ...this.data };
    }
  }
});

Vue.component("part1-of-form", {
  template: `
<div>
  First name:<input v-model="data.firstName"></input>
</div>
`,
  props: {
    data: Object
  }
});

Vue.component("part2-of-form", {
  template: `
<div>
  Second name:<input v-model="data.secondName"></input>
</div>
`,
  props: {
    data: Object
  }
});

new Vue({
  el: "#app",
  data: {
    data: {
      firstName: null,
      secondName: null
    }
  }
});
```
