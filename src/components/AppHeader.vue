<script>

export default {
    data() {
        return {
            selector: 0,

            imgName: "dc-logo.png",

            arrayNav: [
                "Characters",
                "Comics",
                "Movies",
                "TV",
                "Games",
                "Collectibles",
                "Videos",
                "Fans",
                "News",
                "Shop",
            ]
        }
    },

    methods: {
        getImgLogo(imgPath) {
            return new URL(imgPath, import.meta.url).href;
        },

        moveSelector(index) {
            this.selector = index;
        }
    }
}

</script>

<template>

    <div class="container">
        <section>

            <div>
                <img :src="getImgLogo(`../assets/img/${this.imgName}`)" alt="">
            </div>

            <nav>
                <ul class="d-flex">
                    <li v-for="(link, index) in arrayNav" :key="index" :class="{ 'active': this.selector == index }"
                        @click.prevent.stop="moveSelector(index)">
                        <a href=""> {{ link }} </a>
                    </li>
                </ul>
            </nav>

        </section>
    </div>

</template>


<style lang="scss" scoped>
@use "../styles/parziali/variabiles.scss" as *;

img {
    max-width: 70px;
}

nav {
    width: 60%;

    .d-flex {
        display: flex;
        justify-content: space-between;
    }

    ul {
        height: 100px;

        .active {
            color: $primary-color;
            border-bottom: 4px solid $primary-color;
        }

        li {
            line-height: 100px;

            cursor: pointer;
        }

    }


}


section {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>