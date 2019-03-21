<template>
    <div>
        <div v-for="comment in comments" v-bind:key="comment.id">
             <h3 id='comment' v-on:click="boxx">
               <i class="fas fa-comments"></i>
            </h3>
            <div id="box">
                <p>{{comment.comments}}</p>
            </div>
            
            <!-- <ul><li>{{comment.comments}}<li></ul> -->
        </div>  
    </div>
</template>

<script>
export default {
    name: 'Comment',
    props: ['comments'],
    methods:{
        boxx(){
            // this.style.display = 'block'
        }
    }
}
</script>

<style scoped>
    
    #comment:active{
       color: dodgerblue;
    }
    #comment{
        float: left;
        margin: 35px;
        margin-top: 100px
    }
    #box{
        margin: 5px;
        background-color: beige;
        display: inline-block;
        /* display: block; */
    }

</style>



