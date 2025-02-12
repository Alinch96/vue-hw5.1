<template>
    <ul class="raspberry-list">
        <raspberry-item v-for="raspberry in raspberries" :key="raspberry.id" :raspberry="raspberry"/>
    </ul>
</template>

<script>
import RaspberryItem from './RaspberryItem.vue';

export default {
    name: "RaspberryList",
    components: {
        RaspberryItem
    },
    props: {
        raspberries: {
            type: Array,
            required: true
        }
    }
}
</script>

<style lang="scss" scoped>

.raspberry-list {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(300px, 1fr));
    gap: 20px;
    padding: 20px;
    list-style: none;
}

</style>