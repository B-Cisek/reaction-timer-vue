<template>
  <p class="time">Reaction time: {{ score }} ms</p>
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
            this.rank = 'Ninja Fingers!'
        } else if (this.score < 400) {
            this.rank = 'Rapid Reflexes'
        } else {
            this.rank = 'Snail pace...'
        }
    }
}
</script>

<style>
    .time {
        font-weight: 700;
        font-size: 2rem;
        color: crimson;
    }

    .rank {
        font-weight: 700;
        font-size: 1.5rem;
        color: #0faf87;
    }
</style>