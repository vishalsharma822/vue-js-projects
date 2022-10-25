<template>
    <h1 v-if="show">IF-SHOW = true</h1>
    <h2 v-else> Else shown</h2>
</template>
<script>
    export default{
        name : 'TwoIfElse',
        data(){
            return {
                show : false
            }
        }
    }
</script>