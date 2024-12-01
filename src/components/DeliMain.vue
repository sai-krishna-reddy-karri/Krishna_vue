<template>
    <div>
        <div v-for="items of items" :key="items.id">
            <DeliItem :items=items />
        </div>
    </div>
</template>

<script>
import DeliItem from './DeliItem.vue';
export default{
    name:'DeliMain',
    props:{
        items:Array
    },
    components:{
        DeliItem
    }
}
</script>

<style scoped>
div{
    text-align: center;
}
</style>