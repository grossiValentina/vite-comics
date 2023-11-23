<script>
export default {
    data() {
        return {
            headerLink: [
                {
                    title: "CHARACTERS"
                },
                {
                    title: "COMICS"
                },
                {
                    title: "MOVIES"
                },
                {
                    title: "TV"
                },
                {
                    title: "GAMES"
                },
                {
                    title: "COLLECTIBLES"
                },
                {
                    title: "VIDEOS"
                },
                {
                    title: "FANS"
                },
                {
                    title: "NEWS"
                },
                {
                    title: "SHOP"
                },

            ]

        }
    }

}
</script>


<template>
    <div class="wrapper">
        <div class="container">
            <div class="logo">
                <img src="../assets/img/dc-logo.png" alt="logo">
            </div>
            <ul class="list">
                <li v-for="link in headerLink"><a href="">{{ link.title }}</a></li>
            </ul>
        </div>
    </div>
</template>


<style scoped lang="scss">
@use "../style/partials/variables" as *;


.wrapper {
    padding: 1rem 0;
    background-color: $white;

    .container{
        justify-content: space-between;
    }

    .logo {

        img {
            width: 3.5rem;
        }
    }

    .list {
        display: flex;
        list-style: none;
        gap: 1rem;
        margin: 1rem;

        a {
            text-decoration: none;
            color: $black;
            font-size: .6rem;

            &:hover {
                background-color: $blue;
            }
        }

    }

}
</style>