<template>
    <div>
        <h3> {{ data.name }}</h3>
        <h3>{{ data.email }}</h3>
        <button v-on:click="getData(data.name)">Click Me</button>
    </div>
</template>

<script>
export default {
    name:'UserPage',
    props:{
        data:Object,
        getData : Function //function to get the user details from API or any other source
    },
   
}
</script>