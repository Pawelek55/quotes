<template>
    <div class="col-md-4 col-lg-3">
        <div class="panel panel-default">
            <div  class="panel-body box">
                <slot></slot>
            </div>
        </div>
    </div>  
</template>

<script>
    export default {
        props: ['quotes'],
    }
</script>


<style>
    .box{
        font-family: 'Arizonia', cursive;
        font-size: 20px;
        color: #0f0;
    }
    .box:hover{
        cursor: pointer;
        background-color: rebeccapurple; 
    }

</style>



