<template>
  <div id="nav">
    <router-link to="/">Home</router-link> |
    <router-link to="/about">About</router-link>
    <!-- <button @click="goToAbout">About 2</button>
    <div>{{ age }}</div>
    <input v-model="age" type="text"> -->
    <!-- <ul>
      <li v-for="(item, key) in fruits" :key="key">
        The price for {{ item.name }} is {{ item.price }} == 
        {{ `The price for ${item.name} is ${item.price}` }}
      </li>
    </ul>
    <ul>
      <li v-for="(item, key) in veggies" :key="key">
        The price for {{ item.name }} is {{ item.price }} == 
        {{ `The price for ${item.name} is ${item.price}` }}
      </li>
    </ul> -->
  </div>
  <router-view/>
</template>

<script>

import { ref } from 'vue'

export default {
  setup () {
    const ctr = ref(0)
    const veggies = ref([
      { name: 'repolyo', price: 212 },
      { name: 'pipino', price: 323 },
      { name: 'carrots', price: 11 }
    ])
    
    function test () {
      console.log('Heyyyyyyyyyy')
    }

    return {
      ctr,
      veggies,
      test
    }
  },
  data () {
    return {
      age: 0,
      fruits: [
        { name: 'apple', price: 100 },
        { name: 'orange', price: 200 },
        { name: 'banana', price: 159 }
      ]
    }
  },
  methods: {
    goToAbout () {
      this.$router.push({ name: 'About' })
    }
  }
}
</script>


<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;
}

#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
