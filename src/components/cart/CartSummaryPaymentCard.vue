<template>
    <div class="cart-item-card">
        <h3>Cart Total: ${{cart_total.toFixed(2)}}</h3>
        <button class="view-product-button">Pay credit Card</button>
    </div>
</template>

<script>
export default {
    props:['products'],
    computed:{
        cart_total(){
            return this.$store.getters.cartTotal()
        }
    },
    data() {
        return {
            
        };
    },
    mounted() {
        
    },
    methods: {
        
    },
};
</script>

<style lang="scss" scoped>

</style>