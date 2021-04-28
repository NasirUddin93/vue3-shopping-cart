<template>
    <div>
        <h1>Your Cart</h1>
        <CartItemCard 
        v-for="product in products"
        :key="product.id"
        :product="product"
        />
        <CartSummaryPaymentCard
        :products="products"
        />
        
       
    </div>
</template>

<script>
import CartItemCard from '../components/cart/CartItemCard'
import CartSummaryPaymentCard from '../components/cart/CartSummaryPaymentCard'

export default {
    components:{
        CartItemCard,
        CartSummaryPaymentCard,
    },
    data() {
        return {
            
        };
    },
    computed:{
            products(){
            return this.$store.getters.cartItems 
        }
    },
    mounted() {

    },
    methods: {
        
    },
};
</script>

<style lang="scss">

</style>