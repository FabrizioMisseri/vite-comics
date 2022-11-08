<script>

export default {
    data() {
        return {
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
                <ul class="d-flex" v-for="(link, index) in arrayNav">
                    <li><a href=""> {{ link }} </a></li>
                </ul>
            </nav>

        </section>
    </div>

</template>


<style lang="scss" scoped>
nav {
    width: 60%;

    .d-flex {
        display: flex;
        justify-content: space-between;
    }
}

section {
    padding: 2rem;
    display: flex;
    justify-content: space-between;
    align-items: center;
}
</style>