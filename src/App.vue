<template>
<div class="mainContainer">
  <div>
    <h1>这里是keepAlive的demo</h1>
    <dynamic-keep-demo/>
  </div>
  <div>
  <h1>这里是父子组件传值的demo</h1>

  <div class="fater">
    <h5>
      father data:
    </h5>
    <button @click="fatherChage">father 改变名字</button>
      <li v-for="(item,index) in person" :key="index">
        {{item}}
      </li>
  </div>
    <label>son data:</label>
    <son-demo :person="person"/>
  </div>
</div>
</template>

<script>
import DynamicKeepDemo from './components/dynamicDemo/DynamicKeepDemo.vue';
import SonDemo from './components/emitDemo/sonDemo.vue';
export default {
  components: { DynamicKeepDemo, SonDemo },
  name: 'App',
  data () {
    return {
      person: {
        name: '木易啊',
        message: '大脸啊',
        food: ['红薯啊'],
      },
    }
  },
  methods: {
    fatherChage (){
      this.person.name = "faterName";
    }
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  margin: 0 auto;
}
.mainContainer{
  display: grid;
  grid-template-columns: 50% 50%;
}
.fater{
  border: 1px solid black;
}

</style>
