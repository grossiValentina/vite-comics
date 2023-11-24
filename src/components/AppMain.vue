<script>
export default {
    data() {
        return {
            menu: [
                {
                    image: "buy-comics-digital-comics.png",
                    title: "DIGITAL COMICS"
                },
                {
                    image: "buy-comics-merchandise.png",
                    title: "CD MERCHANDISE"
                },
                {
                    image: "buy-comics-shop-locator.png",
                    title: "SUBSCRIPTION"
                },
                {
                    image: "buy-comics-subscriptions.png",
                    title: "COMIC SHOP LOCATOR"
                },
                {
                    image: "buy-dc-power-visa.svg",
                    title: "DC POWER VISA"
                },
            ]
        }
    },
    methods: {
        getImageUrl(image) {
            return new URL(`../assets/img/${image}`, import.meta.url).href;
        }
    }
}
</script>


<template>
    <div class="wrapper">

        <div class="container">
            <h2>contenuto da inserire</h2>
        </div>

    </div>

    <div class="container-sm">

        <div v-for="(item, index) in menu" class="list-menu">

            <img :src="getImageUrl(item.image)" alt="">
            <p><a href="">{{ item.title }}</a></p>

        </div>

    </div>

    <div class="wrapper-bg">
        <div class="image-bg">
            <img src="../assets/img/footer-bg.jpg" alt="">
        </div>
    </div>

</template>


<style scoped lang="scss">
@use "../style/partials/variables" as *;

.wrapper {
    height: 5rem;
    background-color: $black;

    .container {
        h2 {
            color: $white;
            margin-top: 1.5rem;
        }
    }

}

.container-sm {
    max-width: 100%;
    display: flex;
    justify-content: center;
    background-color: $blue;


    .list-menu {
        display: flex;
        background-color: $blue;

        img {
            max-height: 5.5rem;
            padding: 1.5rem 0.3rem 1.5rem 2.5rem;
        }

        p {
            font-size: .6rem;
            margin-top: 2.2rem;
            margin-right: 1.5rem;

            a {
                text-decoration: none;
                color: $white;
            }
        }
    }
}
.wrapper-bg{
    width: 100%;
    background-image: url(../assets/img/footer-bg.jpg);
    background-size:cover;
}


</style>