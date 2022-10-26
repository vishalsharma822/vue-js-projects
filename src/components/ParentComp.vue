<template>
<h2> Hello Parent </h2>
<ChildComp :user="users" :getData='getData' :students='students'/>
</template>

<script>
import ChildComp from './ChildComp.vue'
export default {
    name: 'ParentComp',
    components: {
        ChildComp
    },
    data() {
        return {
            users: {
                name: 'vishal',
                email: 'vishal@gmail.com'
            },
            students:[
                    {name:'student 1', email:'email1@gmail.com'},
                    {name:'student 2', email:'email2@gmail.com'},
                ]
        }
    },
    methods: {
        getData(){
            
            return {
                msg : 'hai',
                employee:[
                    {name:'employee 1', email:'employee1@gmail.com'},
                    {name:'employee 2', email:'employee2@gmail.com'},
                ]
            }
        }
    }
}
</script>