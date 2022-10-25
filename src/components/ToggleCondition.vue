<template>
    <h1 v-if="show"> if- condition</h1>
    <h1 v-else> else- condition</h1>
    <button v-on:click="show=!show">Toggle</button>
</template>

<script>
    export default{
        name : 'ToggleCondition',
        data(){
            return { 
                show :true
            }
        }
    }
</script>