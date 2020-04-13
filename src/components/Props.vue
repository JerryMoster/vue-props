<template>
  <div>
    <h2>组件之间的通讯方式：props</h2>
    <h4>姓名：{{name}}</h4>
    <h4>年龄：{{age}}</h4>
    <h4>性别：{{sex}}</h4>
    <h4>{{person}}</h4>
    <button @click="logPerson('李四',22)">调用父组件中的方法</button>
  </div>
</template>

<script>
export default {
  // props: ['name', 'age', 'sex'],
  // props: {  // 可以换一种写法，更加人性化
  //   name: String,
  //   age: Number,
  //   sex: String,
  //   person: Object,
  //   logPerson: Function
  // },
  props: {
    name: { type: String, required: true, default: '张三' },
    age: { type: Number, required: true, default: 0 },
    sex: { type: String, required: true, default: '男' },
    person: { type: Object, required: true },
    logPerson: { type: Function, required: true }
  },
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

  },
  components: {

  }
}
</script>

<style lang="scss" scoped>
</style>
