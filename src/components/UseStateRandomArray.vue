<script>
import { ref } from 'vue'

export default {
  setup () {
    let items = ref([7, 4])
    let addItem = () => {
      const newItem = Math.floor(Math.random() * 10) + 1
      items.value.push(newItem)
    }
    return {
      items,
      addItem
    }
  }
}
</script>

<template>
  <button @click="addItem">
    Add a Number
  </button>
  <ul>
    <li v-for="(item, index) in items" :key="index">
      {{item}}
    </li>
  </ul>
</template>


