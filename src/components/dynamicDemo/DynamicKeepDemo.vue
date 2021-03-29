
// 当前文件为keep-alive使用方法。当使用v-if的时候，条件发生改变时,dom会根据条件的更改重新创建和挂载dom对象。使用keep-alive时，vue会缓存当前dom
// 使得减少dom的创建和挂载操作
<template>
  <button @click="changeActive">点击改变激活对象personName</button>
  <div>
    <keep-son-1 v-if="component1">
    </keep-son-1>
    <keep-son-2 v-else>
    </keep-son-2>
  </div>
  <button @click="changeActive2">点击keepAlive内改变personName</button>
  <div>
    <keep-alive>
      <keep-son-1 v-if="component2"/>
      <keep-son-2 v-else/>
    </keep-alive>
  </div>
</template>

<script>
import KeepSon1 from './keepSon1.vue'
import KeepSon2 from './keepSon2.vue'
export default {
  name: 'DynamicKeepDemo',
  data () {
    return {
      component1: true,
      component2: true
    }
  },
  components: {
    KeepSon1,
    KeepSon2
  },
  methods: {
    changeActive () {
      this.component1 = !this.component1;
    },
    changeActive2 () {
      this.component2 = !this.component2;
    }
  }
}
</script>

<style>

</style>
