<template>
    <h1>Reuse of Compononets</h1>
    <div v-html="myfName + mylName"></div> 
    <!-- html binding 2-way binding -->
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
            ],
            myfName:"<h5>Nasir</h5>",
            mylName:"<h5>Hussain</h5>",
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