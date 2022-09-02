<template>

<div class="container">
    <h1>Menage Tasks</h1>
    <input type="text" ref="task">
<button @click="setTeleport" type="button" class="btn btn-primary">Teleport</button>

<teleport to="body">

    <error-message v-if="teleport">
      <h1>I am from teleport</h1>  
      <button @click="setTeleport" type="button" class="btn btn-primary">Teleport</button>



    </error-message>
    
</teleport>
</div>
</template>

<script>
    import ErrorMessage from "./ErrorMessage.vue";

export default {
    name:"MainComp",
    components:{
    ErrorMessage,

},

    data(){
        return{
            teleport:false
        }
    

    },
        methods:{
            setTeleport(){
                const entervalue = this.$refs.task.value;
                if(entervalue==""){
                    this.teleport = true;
            }
        }
}
}
</script>