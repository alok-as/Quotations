<template>
    <div class="row">
        <app-quote v-for="(quote,index) in quotes" :key="quote" @click.native="deleteQuote(index)">{{quote}}</app-quote>
    </div>
</template>

<script>
import Quote from "./Quote.vue";

export default {
    props:["quotes"],
    components:{
        "app-quote":Quote
    },
    methods:{
        deleteQuote(index){
            this.$emit("quoteDeleted",index);
        }
    }
}
</script>

<style scoped>
.row{
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    grid-column-gap: 1rem;
    grid-row-gap: 1rem;
}

</style>