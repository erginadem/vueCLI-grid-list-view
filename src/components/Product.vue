<template>
    <div class="card card-body product">
        <h4 class="text text-info">{{ name }}</h4>
        <h6 class="text text-danger">${{ price }}</h6>
        <slot></slot>
    </div>
</template>


<script>
    export default {
        props: ['name', 'price']
    }
</script>


<style lang="scss" scoped>

</style>
