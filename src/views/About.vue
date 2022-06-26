<template>
  <div class="about">
    <h1>This is an about page</h1>
    <ul>
      <li v-for="(person, i) in people" :key="i">
        {{ person }}
      </li>
    </ul>
    <input v-model="name" type="text">
    <button @click="addPerson">Add</button>
  </div>
</template>

<script>
  export default {
    name: 'About',
    data () {
      return {
        people: ['Arnold'],
        name: ''
      }
    },
    methods: {
      addPerson () {
        console.log('Add a person')
        this.people.push(this.name)
        this.name = ''
      }
    }
  }
</script>

<style lang="scss" scoped>

</style>