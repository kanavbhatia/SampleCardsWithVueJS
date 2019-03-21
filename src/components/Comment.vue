<template>
    <div>
        <div v-for="comment in comments" v-bind:key="comment.commentId" >
             <h3 id='comment' v-on:click="boxx"> <i class="fas fa-comments"></i> </h3> 
             <!-- logo -->
            <!-- comment box -->
             <div id="boxy" ref="commentBox">
                 <div v-for="c in comment.comments" v-bind:key="c.commentId">
                    <p>{{c}}</p>
                </div>
             </div>
            
            
            <!-- <ul><li>{{comment.comments}}<li></ul> -->
        </div>  
    </div>
</template>

<script>
export default {
    name: 'Comment',
    props: ['comments', 'commentId'],
    methods:{
        boxx(){
            
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
    #boxy{
        margin: 5px;
        background-color: beige;
        display: inline-block;
        width: 300px;
        /* display: block; */
    }
    #overideStyle{
        display: none;
    }

</style>



