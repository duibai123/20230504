<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h1>姓名：{{ person.name }}</h1>
  <h1>年龄：{{ person.age }}</h1>
  <h1>工作：{{ person.job.type }}</h1>
  <h1>薪水：{{ person.job.salary }}</h1>
  <h1>爱好：{{ person.hobby }}</h1>
  <button @click="sayHello">点击</button>
</template>
<script>
// import HelloWorld from './components/HelloWorld.vue'
import { reactive } from 'vue'
export default {
  name: 'App',
  setup() {
    // let name = ref('张三')
    // let age = ref(18 )
    // let job =reactive({
    //   type:'前端工程师',
    //   salary:"30k"
    //aaaaaaa
    // })
    // let hobby=reactive(['抽烟','喝酒','美女'])
    let person = reactive({
      name: '张三',
      age: 18,
      job: {
        type: '前端工程师',
        salary: '30k',
      },
      hobby: ['抽烟', '喝酒', '美女']

    })
    function sayHello() {
      person.name = '李四'
      person.age = 20
      // job.value.type='全栈工程师'
      person.job.type = '全栈工程师'
      person.job.salary = '35k'
      person.hobby[0] = '嫖娼'
    }

    return {
      // name,
      // age,
      sayHello,
      // job,
      // hobby
      person
    }
    // return ()=>{
    //   return h('h',李易桦)
    // }
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
</style>
