<template>
<h1> Foor Loop in vue JS</h1>
<table border="1">
    <tr><td> Cars - Company</td></tr>
    <tr v-for="company in cars" :key="company">
        <td>{{ company }}</td>
    </tr>
</table>
<br /> 

<table border="1">
    <tr><td> Users- Record (Array-of-Objects)</td></tr>
    <tr v-for="student in users" :key="student">
        <td>Name : {{ student.name }} <br>
        Email : {{ student.email }}</td>
    </tr>
</table>
</template>

<script>
export default {
    name: 'ForLoop',
    data() {
        return {
            cars: ['tata', 'maruti', 'volvo', 'audi', 'bmw'],
            users:[
                {
                    name : 'vishal',
                    email : 'vishal@gmail.com'
                },
                {
                    name : 'rahul',
                    email : 'rahul@gmail.com'
                },
                {
                    name : 'ram',
                    email : 'ram@gmail.com'
                }
            ]
        }
    }
}
</script>
