<template>
    <h2>Form-modifier</h2>
    <input type="text" v-model.lazy="res">
    <h2> Data :- {{ res }}</h2>
</template>

<script>
    export default{
        name: 'FomrModifier',
        data(){
            return {
                res :''
            }
        }
    }
</script>