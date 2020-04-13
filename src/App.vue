<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <Props name="张三" :age=18 sex="男" :person="person" :log-person="logPerson" />
    <CustomEvents @btn="deleteP" />
    <p ref="word">我是即将被删除的标签</p>
  </div>
</template>

<script>
import Props from './components/Props.vue'
import CustomEvents from './components/CustomEvents.vue'

export default {
  name: 'App',
  data () {
    return {
      person: {
        name: '张三丰',
        age: 600
      }
    }
  },
  components: {
    Props,
    CustomEvents
  },
  methods: {
    logPerson (name, age) {
      console.log('子组件中点击事件触发父组件中的方法！')
      console.log(`姓名：${name},年龄：${age}`)
    },
    deleteP (text) {
      console.log(text)
      this.$refs.word.remove()
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
p {
  background-color: red;
  color: #fff;
  font-size: 24px;
}
</style>
