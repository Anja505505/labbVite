<template>
  <div class="about">
    <h1>Hitta närmsta Rehab Center!</h1>
    <h2>Skriv in din stad</h2>
    <input v-model="stad" type="text">
    <div v-if="stad === ''">Fyll i!
    </div>
    <div v-else>Det finns ingen Rehab nära dig:/</div>

  </div>
</template>


<script>
export default {
  data(){
    return {
      stad: ''
    }
  }
}
</script>

<style>
@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    text-align: center;
  }
}
</style>
