<script>

export default {
    data() {
        return {
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
    }
}

</script>

<template>

    <div class="container">
        <section>

            <div>
                <img src="" alt="">
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
}
</style>