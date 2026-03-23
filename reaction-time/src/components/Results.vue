<template>
  <div class="results">Reaction time : {{ score }}ms</div>
</template>

<script>
  export default {
    props: ['score']
  }
</script>

<style>
  .results {
    font-size: 24px;
    color: #0faf87;
  }
</style>
