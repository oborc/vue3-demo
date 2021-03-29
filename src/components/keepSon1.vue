<template>
<span>
    这是第二个组件
</span>
</template>

<script>

export default {
  name: 'keepSon2',
  props: {},
  data () {
    return {

    }
  },
  beforeCreate () {
    console.log('before keepAlive2 Components')
  },
  created () {
    console.log('created keepAlive2 Components')
  },
  beforeMount () {
    console.log('before mounted keepAlive2 Components')
  },
  mounted () {
    console.log('after mounted keepAlive2 ')
  },
  unmounted () {
    console.log('keepAlive2 unmounted')
  }
}
</script>
