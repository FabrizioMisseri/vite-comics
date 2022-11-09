<script>

export default {
    AppHeader: "AppHeader",

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
        <header>

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

        </header>
    </div>

</template>


<style lang="scss" scoped>
@use "../styles/parziali/variabiles.scss" as *;

a {
    text-decoration: none;
    color: inherit;
    font-weight: 600;
}

ul {
    list-style: none;
}

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


header {
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>