<template>
    <div class="products">
        <input type="text" v-model="pid">
        <button @click="onSelectPid">Select product</button>
        <hr>
        <nuxt-link to="/products/1">Product 1</nuxt-link>
        <nuxt-link to="/products/2">Product 2</nuxt-link>
    </div>
</template>
<script>
export default {
    data() {
        return {
            pid: null
        }
    },

    methods: {
        onSelectPid() {
            this.$router.push(`/products/${this.pid}`)
        }
    }
}
</script>

