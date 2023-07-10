<template>
    <!-- <h1>Name {{10+20 }}</h1>  basic concept of nterpolation-->
    <div class="container">
        <h3>Name = {{ getName() }}</h3>
        <!-- also send name from here to function(param) ret param -->
        <h3>Contact No = {{ Contact=3165392191 }}</h3>
        <!-- in vue we can change variable value but ! angular -->
        <h3>Qualification = {{ q }}</h3>
        <!-- if you want dynamic qualification then use method and set it as a prop or v--->
        <!-- <h2>All Data = {{getData().contactNo}}</h2> -->
        <button v-on:dblclick="test()">DClick Restart</button>
        <!-- can pass param as well -->
        <!-- <h3 v-on:mouseover="countfunc()">Count Me{{countfunc()}}</h3> -->
        <button v-on:click="countfunc()">Count Me</button>
        <h2>{{ count }}</h2>


    </div>
</template>
<script>
export default {
    name: 'InterpolationPage', // this is the component's name, which will be used in templates
    data() {
        return {
            Contact: "98765432",
            q: "B.Tech",
            getName: function () {
                return "Nasir Hussain"
            },
            count: 1
        }
        

    },
    methods: {
        getData() {
            return {
                name: 'Shabbir Hussain',
                // contactNo:this.q to assign value of other
                ContactNo:3354913900

            }
        },
        test(){
            this.count=0
            
        },
        countfunc(){
            this.count=this.count+1;
        }
    }
}
</script>