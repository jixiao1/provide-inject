<template>
  <div class="one">one组件
    <div>{{value1}}</div>
    <ul class="navs">
      <li v-for="(item,index) in data" :key="index">{{item}}</li>
    </ul>
    <span>{{ value2 }}</span>
  </div>
</template>

<script>
export default {
  inject: {
    message: {},
    data: {},
    value1: {
      default: 'hi'
    },
    value2: {
      from: 'message'
    }
  }
}
</script>

<style lang='scss'>
.one {
  padding: 10px;
  border: 5px solid red;
}
</style>
