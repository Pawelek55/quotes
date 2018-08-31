<template>
    <div>
       <div class="progress-bar" :style="{width: (quoteCount / maxQuotes) * 100 + '%'}"> {{quoteCount}} / {{maxQuotes}}</div>
    </div>
</template>


<script>
    export default {
        props: ['quoteCount', 'maxQuotes'],
        data: function() {
            return {
                progress: 50,     
                
            }
        }
    }
</script>


<style scoped>
    div{
        border: 2px solid #000;
        height: 30px;
        border-radius: 5px;
        box-sizing: content-box;
    }
    .progress-bar{
        background-color: #00f;
        width: 80%;
        border: none;
    }
</style>