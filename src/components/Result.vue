<template>
    {{timer}}<br>
    {{rank}}
</template>


<script>
export default {
    props:['timer'],

    data(){
        return{
            rank: null,
            slow: 'Slow rank',
            medium: 'Normal rank',
            fast: 'Fast rank'
        }
    },

    mounted(){
        if(this.timer < 390){this.rank = this.fast}
        else if(this.timer > 390 && this.timer < 500){this.rank = this.medium}
        else{this.rank = this.slow}
    }
}
</script>


<style scoped>

</style>