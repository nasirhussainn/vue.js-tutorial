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
        <h3>New Data = {{ getData() }}</h3>

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
            }
        }
    },
    methods: {
        getData() {
            return {
                name: 'Shabbir Hussain',
                // contactNo:this.q to assign value of other
                ContactNo:3354913900

            }
        }
    }
}
</script>