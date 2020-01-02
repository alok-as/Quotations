<template>
  <div class="container">
    <app-header :quoteCount="quotes.length" :maxQuotes="maxQuotes"></app-header>
    <app-new-quote @quoteAdded="newQuote"></app-new-quote>
    <app-quote-grid :quotes="quotes" @quoteDeleted="deleteQuote"></app-quote-grid>
    <div class="info">Info: Click on Quote to delete it.</div>
  </div>
</template>

<script>
import Header from "./components/Header";
import QuoteGrid from "./components/QuoteGrid";
import NewQuote from "./components/NewQuote";

export default {
  data(){
    return {
      maxQuotes:10,
      quotes:[
        "Just a Quote to see something"
      ]
    };
  },
  methods:{
    newQuote(quote){
      if(this.quotes.length>=this.maxQuotes){
         return alert("Delete Some Quotes First");
      }
      else{
        this.quotes.push(quote);
      }
    },
    deleteQuote(index){
      this.quotes.splice(index,1);
    }
  },
  components:{
    "app-header":Header,
    "app-quote-grid":QuoteGrid,
    "app-new-quote":NewQuote
  }
}
</script>

<style>
.container{
  width: 85%;
  margin: 0 auto;
}

.info {
  margin-top: 4rem;
  text-align: center;
  background-color:aqua;
  padding: 1rem; 
}

</style>
