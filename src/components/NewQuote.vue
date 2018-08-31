
<template>
    <div class="row">
       <form>
        <div class="col-md-6 col-md-offset-3 form-group">
           <h3>Your quote</h3>
            <textarea class="form-control" rows="3" v-model="quote"></textarea>
        </div>
        <div class="col-md-6 col-md-offset-3 form-group">
            <button @click.prevent="createNew">Add Quote</button>
        </div>
       </form>
    </div>
    
</template>

<script>
    export default {
        data: function(){
            return {
                quote: ''
            }
        },
        methods: {
            createNew(e) {
/*                console.dir(e.target.previousElementSibling.value)
                addQuoteMain.$emit('quoteWasAdding', e.target.previousElementSibling.value)
                e.target.previousElementSibling.value = '' it is the same but writting in vue.js: this.quote = '';*/ 
                this.$emit('quoteWasAdding', this.quote);
                this.quote = '';
            }
        },
    }
</script>


<style>
    h3{
        margin-top: 50px;
    }
        textarea{
        height: 100px;
        width: 100%;
        margin: auto;
        border: 1px solid black;
        border-radius: 10px;
    }
        button{
        width: 100px;
        background-color: skyblue;
        border-radius: 5px;
        border: 1px solid black;
    }

</style>
