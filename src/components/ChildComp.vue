<template>
<H2> Child Component</H2>
<h3>{{ user.name }}</h3>

<ul>
    <h5>Data coming from Parent - Array</h5>
    <li v-for="student in students" :key="student">
        {{ student.name }}
    </li>
</ul>

<button v-on:click="getData(),showHide()"> Get Student From Parent</button>
<div class="showHide">
    <h5>Data coming from Parent - Array of object</h5>
    <ol>
        <li v-for="employee in getData().employee" :key="employee">
            {{ employee.name }}
        </li>
    </ol>
</div>
</template>

<script>
export default {
    name: 'ChildComp',

    props: {
        user: Object,
        getData: Function,
        students:Array
    },
    methods:{
        showHide(){
            document.querySelector('.showHide').style.display = "block";
        }
    }
}
</script>

<style>
    .showHide{
        display: none;
    }
</style>
