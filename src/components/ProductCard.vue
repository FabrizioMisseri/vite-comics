<script>
export default {
    ProductCard: "ProductCard",

    data() {
        return {

        }
    }
}
</script>

<template>

    <div class="card">
        <div class="content"></div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/parziali/variabiles" as *;

.card {
    width: calc(100% / 6);
    padding: 1rem;
    // debug

    .content {
        //debug
        background-color: $color-white;
        height: 100px;
    }
}
</style>