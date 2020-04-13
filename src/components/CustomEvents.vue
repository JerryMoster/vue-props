<template>
  <div>
    <h2>自定义事件的通讯方式</h2>
    <button @click="btn">点击删除父组件中的 p 标签</button>
  </div>
</template>

<script>
export default {
  data () {
    return {

    }
  },
  computed: {

  },
  created () {

  },
  mounted () {

  },
  watch: {

  },
  methods: {
    btn () {
      // 告诉父组件，我点击了按钮，触发率这个事件
      this.$emit('btn', { name: '哈哈哈哈哈', sex: '男' })
    }
  },
  components: {

  }
}
</script>

<style lang="scss" scoped>
</style>
