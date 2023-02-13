<template>
<div class="form">
<form @submit.prevent="submitForm"></form>
<div class="form-group">
<label for="exampleFormControlInput1">Email adress</label>
<input type="email" class="form-control" id="exampleFormControlInput1" placeholder="name@example.com" v-model="email"/>
</div>
<div class="form-group">
<label for="exampleFormControlSelect1">Vilken specialist behöver du träffa?</label>
<select class="form-control" id="exampleFormControlSelect1" v-model="specialist">
<option>Sjukgymnast</option>
<option>Rehabilitering</option>
<option>Kiropraktor</option>
</select>
</div>
<div class="form-group">
<label for="exampleFormControlTextarea1">Beskriv kort dina problem</label>
<textarea class="form-control" id="exampleFormControlTextarea1" rows="3" v-model="description"></textarea>
</div>
<button @click="onClick" type="submit" :disabled="!isFormValid">Skicka in</button>

</div>
</template>

<script>
export default {
    data(){
        return {
            email: '',
            specialist: '',
            description: ''
        }
    },
    computed: {
        isFormValid(){
            return this.email && this.specialist && this.description
        }
    },
    methods:{
        onClick(){
            return alert('Tack! Vi hör av oss inom 2 arbetsdagar')
        }
    }
}
</script>


<style>
.form{
    margin-top: 30px;
    margin-left: auto;
    margin-right:auto;
    width: 400px;
    text-align: center;
}
</style>
