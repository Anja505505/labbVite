<script setup>
import heroText from '../components/heroText.vue'
import rehabOptions from '../components/rehabOptions.vue'
import bootForm from '../components/bootForm.vue'
</script>

<template>
<heroText/>
<h2 class ="title">{{ description }}</h2>
<rehab-options v-for="rehab in rehabs" :key="rehab.id" :offer="rehab"/>
<bootForm/>
</template>

<script>
export default {
    data(){
        return {
        description: "Hitta rätt rehabilitering för dig",
        rehabs: []
    }
},

components: {'rehab-options': rehabOptions },
mounted(){
    this.fetchData()
},
methods: {
    async fetchData(){
        const response = await fetch('rehab.json')
        const val = await response.json()
        this.rehabs = val
    }
}



}</script>

<style>
.title{
    text-align: center;
    font-size: 25px;
}
</style>
