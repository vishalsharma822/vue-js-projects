<template>
<h2>Simple Form</h2>
<ul>
    <li v-for="err in error" :key="err">
        {{ err }} shoud not be blank
    </li>
</ul>
{{ formData }}
<form>
    <label for="email">Enter your email:</label>
    <input type="email" id="email" v-model="formData.email">
    <br /><br />

    <label for="password">Enter your password:</label>
    <input type="password" id="password" v-model="formData.password">
    <br /><br />

    <h3>Country Selection</h3>
    <select v-model="formData.country">
        <option value="india">india</option>
        <option value="USA">USA</option>
        <option value="Japan">Japan</option>
    </select>
    <br /><br />

    <h3>Choose Gender(Radio)</h3>
    <label for="male">Male</label>
    <input type="radio" name="gender" id="male" value="Male" v-model="formData.gender">
    <label for="female">Female</label>
    <input type="radio" name="gender" id="female" value="Female" v-model="formData.gender">
    <br /><br />

    <h3>Select Technology (Checkbox)</h3>
    <label for="java">Java</label>
    <input type="checkbox" id="java" value="java" v-model="formData.technology">
    <label for="php">Php</label>
    <input type="checkbox" id="php" value="php" v-model="formData.technology">
    <label for="nodejs">NodeJs</label>
    <input type="checkbox" id="nodejs" value="nodejs" v-model="formData.technology">
    <br /><br />
    <button type="button" v-on:click="getFormData">SignUp</button>
</form>
</template>

<script>
export default {
    name: 'SimpleForm',
    data() {
        return {
            formData: {
                email: '',
                password: '',
                country: '',
                gender: '',
                technology: []
            },
            error:[]
        }
    },
    methods: {
        getFormData() {
            let item;
            this.error = [];
            for(item in this.formData){
                if(this.formData[item] === '' || this.formData[item].length === 0){
                    this.error.push(item);
                    console.log(this.error);
                }
                if(this.error.length === 0){
                    alert('data submitted');
                }
            }
            //console.log(this.formData);

        }
    }
}
</script>
