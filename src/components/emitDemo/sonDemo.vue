<template>
    <li v-for="(item,index) in person" :key="index">
        {{item}}
    </li>
    <button @click="changeName">son change name</button>
</template>
<script>
export default {
    name:'sonDemo',
    data(){
        return{

        }
    },
    props:{
        person:{
            type: Object
        },
        name: {
            type: String
        }
    },
    methods:{
        changeName(){
            this.person.name = "sonName";
        }
    }
}
</script>