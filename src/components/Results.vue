<template>
  <p>Timer Speed {{score}} ms</p>
  <p class="rank">{{ rank }}</p>
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
        if (this.score < 250) {
            this.rank = 'Mantap Wir'
        } else if (this.score < 400) {
            this.rank = 'Kecepatan Ngocok'
        } else {
            this.rank = 'Lambat Banget...'
        }
    }
}
</script>

<style>
    .rank {
        font-size: 1.4em;
        color: #0faf87;
        font-weight: bold;
    }
</style>