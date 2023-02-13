
<template>

    <div class="card" style="width: 18rem;">
  <div class="card-body">
    <h5 class="card-title">{{ offer.name }}</h5>
    <p class="card-text">{{ offer.summary }}</p>
    <p class="card-text">{{ offer.price }}</p>
    <a href="#" class="card-link">Boka här!</a>
    <a href="#" class="card-link">Närmsta butik</a>
  </div>
</div>

</template>
<script>
export default {
    props: {
        offer:{
            required: true,
            type: Object
        }
    }
}
</script>


<style>
.card {
    margin: 0 auto;
    float: none;
    margin-top: 30px;
}

</style>
