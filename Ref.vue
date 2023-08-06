<template>
    <h3>Refs in Vue.js</h3>
    <input type="text" name="ref" id="myref" ref="input">
    <button v-on:click="getData()">Click Me</button>
</template>
<script>
export default {
    name:"RefVue",
    methods:{
        getData(){
            let val=this.$refs.input.value
            alert(val)
            this.$refs.input.focus()
            this.$refs.input.style.color="red"
        }
    }
}
</script>