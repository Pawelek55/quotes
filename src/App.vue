<template>
    <div class="container">
       <div class="row">
       <div class="col-md-12">
            <h1>Quotes Added</h1>
            <appHeader :quoteCount="quotes.length" :maxQuotes="maxQuotes"></appHeader>
       </div>
      <appNewQuote @quoteWasAdding="newQuote"></appNewQuote>
       <addingText :quotes="quotes" @quoteDelated="quoteWasDelated" ></addingText>
       <div class="row">
           <div class="col-md-12 text-center">
               <div class="alert alert-info" v-if="quotes.length < maxQuotes">Info: Click on a Quote to delate it</div>
               <div class="alert alert-info" v-else>You don't have space on new quotes, please click on a Quote to delate it</div>
           </div>
       </div>
        </div>
    </div>
</template>

<script>
    import Header from './components/Header.vue';
    import Text from './components/Text.vue';
    import NewQuote from './components/NewQuote.vue';
    export default {
        data: function() {
            return {
                quotes: ['Just a Quote to see somthing'],
                maxQuotes: 10
                
            }
        },
        methods: {
            newQuote(quote){
                if (this.quotes.length >= this.maxQuotes){
                    return alert("You don't have space");
                }
                this.quotes.push(quote);
              
            },
            quoteWasDelated(index){
                this.quotes.splice(index, 1)
            }
        },
        components: {
            appHeader: Header,
            addingText: Text,
            appNewQuote: NewQuote,
        },
    }

</script>


