<template>
  <div id="app">
    <input type="text" ref="in">
    <button @click="clickHandler">添加</button>
    <Wrap></Wrap>
  </div>
</template>

<script>
import Wrap from './components/Wrap.vue'
export default {
  name: 'App',
  components: {
    [Wrap.name]: Wrap
  },
  data () {
    return {
      list: [1, 2, 3]
    }
  },
  provide () {
    return {
      message: 'hello world',
      data: this.list
    }
  },
  methods: {
    clickHandler () {
      if (this.$refs.in.value) {
        this.list.push(this.$refs.in.value)
        this.$refs.in.value = ''
      }
    }
  }
}
</script>

<style lang="scss">
#app {
}
</style>
