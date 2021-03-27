<template>
<span>
    这是第一个组件
</span>
</template>

<script>

export default {
    name: 'keepSon1',
    props:{},
    data(){
        return{

        }
    },
    beforeCreate(){
        console.log("before keepAlive1 Components");
    },
    created(){
        console.log("created keepAlive1 Components");
    },
    beforeMount(){
        console.log("before mounted keepAlive1 Components");
    },
    mounted(){
        console.log("after mounted keepAlive1 ");
    },
    unmounted(){
        console.log("keepAlive1 unmounted");
    }
}
</script>
