<template>
  <div class="home">
    <input type="number" @change="changeYear" v-model="year">
    {{res}}
  </div>
</template>

<script>
import calculateNewYear from '../helper'
export default {
  name: 'Home',
  components: {
  },
  data () {
    return {
      year: 2021,
      res: {}
    }
  },
  created () {
    this.res = calculateNewYear(this.year)
  },
  methods: {
    changeYear () {
      this.res = calculateNewYear(this.year)
    }
  }
}
</script>
