<template>
  <div class="container">
    <appHeader :maxQuote="maxQuote" :quoteCount="quotes.length"></appHeader>
    <appNewQuote @addedQuote="newQuote"></appNewQuote>
    <appQuoteGrid :quotes="quotes" @quoteDeleted="deleteQuote"></appQuoteGrid>
    <div class="row">
      <div class="col-sm text-center mt-4">
        <div class="alert alert-info">Info: Click to delete a quote.</div>
      </div>
    </div>
  </div>
</template>

<script>
  import QuoteGrid from './components/QuoteGrid.vue';
  import NewQuote from './components/NewQuote.vue';
  import Header from './components/Header.vue';

  export default {
    data : function () {
      return {
        quotes : [
          'This is first quote'
        ],
        maxQuote : 10
      };
    },
    methods : {
      newQuote(quote){
        if (this.quotes.length >= this.maxQuote)
        {
          return alert("Please, Delete some of the quote first.")
        }
        this.quotes.push(quote);
      },
      deleteQuote(index){
        this.quotes.splice(index, 1);
      }
    },
    components : {
      appQuoteGrid : QuoteGrid,
      appNewQuote : NewQuote,
      appHeader : Header,
    }
  }
</script>

<style scoped>
</style>
