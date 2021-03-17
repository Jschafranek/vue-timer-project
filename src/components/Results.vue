<template>
  <p class="time">Reaction Time: <strong>{{score}}</strong> ms</p>
  <p class="rank">{{rank}}</p>
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
        if(this.score < 250) {
            this.rank = `Very Fast!!`
        } else if (this.score < 300) {
            this.rank = `Pretty Fast.`
        } else if(this.score < 400) {
            this.rank = `Getting Faster..`
        }else {
            this.rank = `Bruh...`
        }
    }
}
</script>

<style>

.time{
    font-size: 24px;
}

.rank {
    font-style: initial;
    font-family: 'Courier New', Courier, monospace;
    color: rgb(245, 0, 0);
    font-size: 30px;
    font-weight: 200;
    
}

</style>