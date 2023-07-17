<template>
    <h2>This is child Page</h2>
    <h4>{{ name }}</h4>
    <h4>{{user.name}}</h4>
    <button v-on:click="getEmail()">CLick Me</button>

</template>
<script>
export default{
    name: "ChildPage",
    props:{
        name:String,
        user:Object,
        getEmail:Function,   
    }
}

</script>