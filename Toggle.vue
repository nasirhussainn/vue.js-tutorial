<template>
    <h3>My Article</h3>
    <p v-if="show">
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non laboriosam saepe ab praesentium quos eos dolor alias veniam, <button type="button" v-on:click="show=!show">Read More</button>
    </p>
    <p v-else>
        Lorem ipsum dolor, sit amet consectetur adipisicing elit. Non laboriosam saepe ab praesentium quos eos dolor alias veniam,atione laborum obcaecati iste repellendus ea dolores natus quidem aliquam nobis accusantium? Vitae, quas voluptate iusto possimus, officiis laboriosam voluptas similique libero assumenda illo voluptates. Cum quam numquam quis impedit dicta doloribus reiciendis, temporibus iusto voluptatem aliquam exercitationem quia ex sit natus. Ducimus fugiat soluta ullam amet perferendis velit, optio eaque debitis, veritatis enim ratione ipsa? Quaerat modi molestiae sit id, alias eaque deserunt molestias quibusdam consectetur esse dicta cum earum error doloribus ducimus sapiente nostrum! Porro doloremque nisi aut sed quaerat. <button type="button" v-on:click="show=!show">Read More</button>  
    </p>
  
</template>

<script>
export default {
    name:'ToggleView',
    data(){
        return{
            show:true,
        }
    }
}
</script>