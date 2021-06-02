<template>
    <div><span :class="{ 'top-most-item': index == 0 }">{{ item }}</span></div>
</template>
<script>
export default {
    props: ['index','item'],
    data: function() {
        return {
            myItem: null
        }
    },
    mounted() {
        this.myItem = this.item;
    }
}
</script>
