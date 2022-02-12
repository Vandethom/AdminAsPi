<template>
  <div class="card">
    <h3 class='card_title'>{{ card_title }}</h3>
    <p class='card_data'>{{ card_data }}</p>
    <p class='card_legend'>{{ card_legend }}</p>
  </div>
</template>

<script>
export default {
    name: 'Card',
    
    props: {
      card_title: String,
      card_data: Number,
      card_legend: String
    }
}
</script>

<style lang='scss'>
  .card {
    width: 250px;
    height: 150px;
    border-radius: 3px;
    margin: 0 24px 20px 0;
    background: linear-gradient(0.20turn, #7d76fd, #1e2485);

    * {
      padding-left: 10px;
      font-family: 'Vollkorn';
    }

    .card_title {
      font-size: 20px;
    }

    .card_data {
      font-size: 38px;
      font-weight: bold;
      margin: 0;
    }

    .card_legend {
      font-size: 15px;
    }
  }
</style>