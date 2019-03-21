<template>
    <div>
        <div v-for="like in likes" v-bind:key="like.LikeId" v-on:click="$emit('inc-like',like.likeId)">
             <h3 id='like'>
               {{like.likes}} 
               <i class="fas fa-heart"></i>
            </h3>
            <!-- <ul><li>{{like.comments}}<li></ul> -->
        </div>  
    </div>
</template>

<script>
export default {
    name: 'like',
    props: ['likes','LikeId'],
    methods:{
        
    }
}
</script>

<style scoped>
    #like:active{
       color: red;
    }
    #like{
        float: left;
        margin: 35px;
        margin-top: 100px
    }

</style>



