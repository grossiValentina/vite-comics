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
    padding: .5rem 0;
    background-color: $white;

    .container{
        justify-content: space-between;
    }

    .logo {

        img {
            width: 3rem;
        }
    }

    .list {
        display: flex;
        list-style: none;
        gap: 1rem;
        margin: 1rem;

        li{
            height: 100%;


             a{
                 text-decoration: none;
                 color: $black;
                 font-size: .6rem; 
                 position: relative;

                 &::after{
                     content: "";
                     height: .3rem;
                     width: 100%;
                     background-color: $blue;
                     position: absolute;
                     left: 0;
                     bottom: 0;
                   }
               }
        }
    }
}
</style>