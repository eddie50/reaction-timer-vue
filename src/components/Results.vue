<template>
  <p >Reaction Time : {{ scoree }} ms</p>
  <p class="rank"> {{ rank }}</p>
</template>

<script>
export default {
    props:['scoree'],
    data(){
        return{
            rank:null,

        }
    },
    mounted(){
        if(this.scoree < 250) this.rank = 'Ninja Fingers'
        else if(this.scoree < 400) this.rank = 'Rapid Refelexes'
        else this.rank = 'Snail Pace... :('
    }
}
</script>

<style>
    .rank{
        font-size: 1.4em;
        color:#0faf87 ;
        font-weight: bold;
    }
</style>