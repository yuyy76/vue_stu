<template>
  <div id="app">
    {{ hello }}

    <componentA v-for="(v1,k1) in objList" :key="key">

    </componentA>

    <ul>
      <li v-for="(item,index) in list"> 
        {{ item.name }} - {{item.price }}
      </li>
    </ul>

    <ul>
      <li v-for="(v1,k1,i1) in objList">
          {{v1}} = {{k1}} = {{i1}}
      </li>
    </ul>
  </div>
</template>

<script>

import componentA from './components/a.vue'

export default {
  components: {componentA},
  data () {
    return {
      hello: '<span>world</span>',
      list: [
        {
          name: 'apple',
          price: 30
        },
        {
          name: 'orange',
          price: 40
        }
      ],
      objList: {
          name: 'apple',
          price: 30,
          color: 'red',
          weight: 20
      }
    }
  }
}
</script>

<style>
html {
  height: 100%;
}

body {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 100%;
}

#app {
  color: #2c3e50;
  margin-top: -100px;
  max-width: 600px;
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  text-align: center;
}
</style>
