<script>
import {ref} from 'vue'

export default {
  setup(){
    return { 
      name: ref({first: '', last: ''})
    }
  }
}
</script>

<template>
  <form>
    <input type="text" v-model="name.first" />
    <input type="text" v-model="name.last" />
    <h2>Your first name is - {{name.first}}</h2>
    <h2>Your last name is - {{name.last}}</h2>
  </form>
</template>

