<template>
  <div>
    <ul>
      <li  @longtap="delOne(index)"  v-for="(item, index) in messages" :key="index">
        {{item}}
      </li>
    </ul>
  </div>
</template>

<script>

export default {
  data:function () {
    return {
      messages: ['你好吗？','不好呀'] 
    }
  },
 
  methods: {
    delOne(index){
      wx.showModal({
        title:"警告",
        content:"你确定删除吗？"
      })

      }
    }
}

</script>

<style scoped>

</style>
