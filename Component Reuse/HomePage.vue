<template>
    <h1>Reuse of Compononets</h1>
    <div class="container">
        <ul>
            <li v-for="item in user" :key="item">
                <UserPage :data="item" :getData="getData"/>
                <!-- {{item.name }} -->
            </li>
        </ul>
    </div>
</template>
<script>
import UserPage from './UserPage.vue'
export default {
    name: "HomePage",
    components: {
        UserPage
    },
    methods:{
        getData(name){
            alert(name);
        }
    },
    data() {
        return {
            user: [
                { name: "Nasir", email: "nasir@g.com" },
                { name: "Yasir", email: "yasir@g.com" },
                { name: "Basir", email: "basir@g.com" },
                { name: "Qasir", email: "qasir@g.com" },
            ]
        }
    },
  
}
</script>
<style>
.container {
    display: flex;
    align-items: center;
    justify-content: center;
}
</style>