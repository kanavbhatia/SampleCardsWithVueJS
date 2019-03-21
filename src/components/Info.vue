<template>
    <div>
        <div v-for="info in infos" v-bind:key="info.id">
            <h3>{{info.class}}</h3>
            <h4>{{info.line}}</h4>
        </div>  
    </div>
</template>

<script>
export default {
    name: 'Info',
    props: ['infos']
}
</script>

<style scoped>
    img{
        height: 250px;
        width: 250px;
    }

</style>


