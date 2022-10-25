<template>
    <h1 v-if="msg ==='if-else'"> msg :{{ msg }}</h1>
    <h1 v-else> msg :{{ elseMsg }}</h1>
</template>

<script>
    export default{
        name : "IfElse",
        data(){ 
            return {
                msg : "if-else",
                elseMsg : "else-msg"
            }
        }
    }
</script>