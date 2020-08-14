<script>
import { ref, computed } from 'vue'

export default {
  setup () {
    let count = ref(0)
    const double = computed(() => {
      return count.value * 2
    })
    return {
      count,
      double
    }
  },

  data(){
    return {
      count: 0
    }
  },
  computed: {
    double() {
      return this.count * 2
    }
  }
}
</script>

<template>
  <p>You clicked half of {{double}} times</p>
  <button @click="count++">
    Click me
  </button>
</template>



<style scoped>

</style>
vbase-3