<template>
    <div class="row">
        <appQuote v-for="(quote, index) in quotes" @click.native="delateQuote(index)">{{quote}}</appQuote>
    </div>
</template>


<script>
    import Quote from './Quote.vue';
    export default {
        props: ['quotes'],
        methods: {
            delateQuote(index) {
                this.$emit('quoteDelated', index)
            }
        },        
        components: {
            appQuote: Quote
        }
    }
    
</script>



