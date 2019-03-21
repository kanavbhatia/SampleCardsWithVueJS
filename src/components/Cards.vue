<template>
    <div>
        <div v-for="card in cards" v-bind:key="card.id" class="box" >
            <photo v-bind:url="card.picURL"/>
            <info v-bind:infos="card.about"/>
            <like v-bind:likes="card.rating" v-bind:likeId="card.id"  v-on:inc-like="$emit('inc-like',card.id)"/>
            <comment v-bind:comments="card.rating" v-bind:commentId="card.id" />
        </div>  
    </div>
</template>

<script>

import Photo from './Photo'
import Info from './Info'
import Like from './Like'
import Comment from './Comment'

export default {
    name: 'Cards',
    props: ['cards'],
    components: {
        Photo,
        Info,
        Like,
        Comment
    }
}
</script>

<style scoped>
    .box{
        height: 500px;
        width: 300px;
        margin: 5px;
        background-color: beige;
        display: inline-block;
        vertical-align: top;
    }
    .box img{
        height: 250px;
        width: 250px;
    }

</style>


