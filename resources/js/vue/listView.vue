<template>
    <div>
        <div v-for="(item, index) in items" :key="index">
            <list-item
                :item="item"
                class="item"
                v-on:itemchanged="$emit('reloadlist')"
                />
        </div>
    </div>
</template>

<script>
import ListItem from "./listItem";
export default {
    components: {ListItem},
    props: ['items']
}
</script>


<style scoped>
.item{
    background-color: #e6e6e6;
    padding: 5px;
    margin-top: 5px;
}

</style>
