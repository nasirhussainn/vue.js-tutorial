<template>
    <h1>Passing Data to Child Data</h1>
    <ChildPage :name="name" :user="user" :getEmail="getEmail"/>
</template>
<script>
import ChildPage from './ChildPage.vue';
export default{
    name:'ParentPage',
    components: {
        // 'ChildPage': ChildPage, //register the child component in this parent page's scope
        ChildPage  //shorthand syntax for above line of code
    },
    data(){
        return{
            name:"Nahida Batool",
            user:{name:"Kashif",email:"kashif@gmail.com"}
        }
    },
    methods: {
        getEmail(){
            alert(this.user.email)
        }
    },
}
</script>