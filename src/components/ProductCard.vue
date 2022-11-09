<script>
import { stringifyStyle } from '@vue/shared';

export default {
    ProductCard: "ProductCard",

    props: {
        text: String,
        imgSrc: String,
    },

    data() {
        return {

        }
    }
}
</script>

<template>

    <div class="card">
        <div class="content">

            <!-- img -->
            <div class="img-box">
                <img :src="imgSrc" alt="">
            </div>
            <!-- / img -->

            <!-- text -->
            <h5>
                {{ text }}
            </h5>
            <!-- / text -->

        </div>
    </div>

</template>

<style lang="scss" scoped>
@use "../styles/parziali/variabiles" as *;

.card {
    width: calc(100% / 6);
    padding: 1rem;
    margin-bottom: 2rem;

    .content {
        h5 {
            text-align: center;
            color: $color-white;
            margin-top: .6rem;
        }


    }
}
</style>