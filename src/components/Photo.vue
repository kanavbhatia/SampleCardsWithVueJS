<template>
    <div>
        <div>
            <img :src="url">
        </div>  
    </div>
</template>

<script>
export default {
    name: 'Photo',
    props: ['url']
}
</script>

<style scoped>
    img{
        height: 250px;
        width: 250px;
    }

</style>


