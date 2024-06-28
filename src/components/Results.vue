<template>
  <p>Reaction time - {{ score }} ms</p>
  <p class="rank">{{ rank }}</p>
</template>

<script>
export default {
  props: ['score'],
  data() {
    return {
      rank : null
    }
  },
  mounted() {
    if (this.score < 200) {
      this.rank = 'incroyable'
    } else if (this.score < 400) {
      this.rank = 'Bon reflexes'
    } else {
      this.rank = 'tu es lent'
    }
  }
}
</script>

<style>
  .rank {
    font-size: 1.4em;
    color: #439b09;
    font-weight: bold;
  }
</style>