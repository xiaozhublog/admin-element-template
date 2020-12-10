<template>
  <div class="home">
    <p>{{ message }}</p>
  </div>
</template>

<script>
export default {
  name: 'Home',
  components: {},
  data() {
    return {
      message: 'Xiaozhublog.com'
    }
  },
  beforeCreate: function() {
    console.group('beforeCreate 创建前状态===============》')
    // this.$el                         undefined
    // this.$data=>[object Object]      undefined
    // this.message=>Xiaozhublog.com    undefined
  },
  created: function() {
    console.group('created 创建完毕状态===============》')
    // this.$el                         undefined
    // this.$data=>[object Object]      已经被初始化
    // this.message=>Xiaozhublog.com    已经被初始化
  },
  beforeMount: function() {
    console.group('beforeMount 挂载前状态===============》')
    // this.$el                         已经被初始化
    // this.$data=>[object Object]      已经被初始化
    // this.message=>Xiaozhublog.com    已经被初始化
  },
  mounted: function() {
    console.group('mounted 挂载结束状态===============》')
    // this.$el                         已经被初始化
    // this.$data=>[object Object]      已经被初始化
    // this.message=>Xiaozhublog.com    已经被初始化
  },
  beforeUpdate: function() {
    console.group('beforeUpdate 更新前状态===============》')
    // 这里指的是页面渲染新数据之前(也就是页面上还没有看到文字或图片)
  },
  updated: function() {
    console.group('updated 更新完成状态===============》')
  },
  beforeDestroy: function() {
    console.group('beforeDestroy 销毁前状态===============》')
  },
  destroyed: function() {
    console.group('destroyed 销毁完成状态===============》')
  },
  methods: {
    // 方法
  }
}
</script>
