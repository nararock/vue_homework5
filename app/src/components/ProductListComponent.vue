<template>
    <div>
        <ProductDetailsComponent v-for="product in products" :key="product.id" :product="product"/>
    </div>
        
</template>

<script>
import ProductDetailsComponent from './ProductDetailsComponent.vue';

    export default {
    data() {
        return {
            products: [
                {
                    id: 1,
                    name: 'Apple',
                    price: 4.55,
                    available: true
                },
                {
                    id: 2,
                    name: 'Plum',
                    price: 3.40,
                    available: false
                },
                {
                    id: 3,
                    name: 'Orange',
                    price: 5.99,
                    available: true
                },
                {
                    id: 4,
                    name: 'Banana',
                    price: 3.49,
                    available: true
                }
            ]
        };
    },
    components: { ProductDetailsComponent }
}
</script>

<style lang="scss" scoped>
    div{
        display: flex;
        flex-direction: column;
        align-items: center;       
    }
</style>