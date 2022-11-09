<script>
import ProductCard from './ProductCard.vue';

export default {
    ProductList: "ProductList",

    components: {
        ProductCard,
    }
}
</script>

<template>
    <main>
        <div class="container d-flex">
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />
            <ProductCard />

        </div>
    </main>
</template>

<style lang="scss" scoped>
@use "../styles/parziali/variabiles" as *;

main {
    padding: 2rem 0;
    background-color: $color-steel;
}
</style>