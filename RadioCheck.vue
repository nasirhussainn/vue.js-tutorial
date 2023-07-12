<template>
    <div class="container">
        <div class="tech">
            <h4>Select the technology</h4>
            <label for="php">PHP</label>
            <input type="checkbox" id="php" value="php" v-model="tech">
            <br>
            <label for="java">Java</label>
            <input type="checkbox" id="java" value="java" v-model="tech">
            <br>
            <label for="python">Python</label>
            <input type="checkbox" id="python" value="python" v-model="tech">
        </div>
        <div class="info">
            <h4>Select Role</h4>
            <label for="std">Student</label>
            <input type="radio" name="intro" id="std" value="Student" v-model="intro">
            <br>
            <label for="dev">Developer</label>
            <input type="radio" name="intro" id="dev" value="Developer" v-model="intro">
        </div>
        <div class="Output">
            <h2>Your Profile</h2>
            <h4>Selected Technologies : {{this.tech}}</h4>
            <h4>Selected Role : {{this.intro}}</h4>
        </div>
    </div>
</template>

<script>
export default{
    name:'RadioCheck',
    data(){
        return{
            tech:[],
            intro:null
        }
    }

}

</script>