<template>
  <p class="results">Reaction time : {{ score }}ms</p>
  <p class="rank">Rank : {{ rank }}</p>
</template>

<script>
  export default {
    props: ['score'],
    data() {
      return {
        rank: null
      }
    },
    mounted() {
      if (this.score < 200) {
        this.rank = 'Ninja'
      } else if (this.score < 300) {
        this.rank = 'Samurai'
      } else if (this.score < 400) {
        this.rank = 'Ronin'
      } else {
        this.rank = 'Snail pace...'
      }
    }
  }
</script>

<style>
  .results {
    font-size: 24px;
    color: #0faf87;
  }
  .rank {
    font-size: 18px;
    color: #444;
  }
</style>
