<template>
  <div class="wrap">wrap组件
    <hr>
    <One></One>
    <hr>
    <Two></Two>
  </div>
</template>

<script>
import One from './One.vue'
import Two from './Two.vue'
export default {
  name: 'Wrap',
  components: {
    One,
    Two
  }
}
</script>

<style lang="scss">

</style>
