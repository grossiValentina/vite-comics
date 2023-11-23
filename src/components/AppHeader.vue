<script>
export default {
    data() {
        return{
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
    <header>
        <div class="logo">
            <img src="../assets/img/dc-logo.png" alt="logo">
        </div>
        <ul class="list">
            <li v-for="link in headerLink"><a href="">{{ link.title }}</a></li>
        </ul>
    </header>
</template>


<style scoped lang="scss">
@use "../style/partials/variables" as *;

   header{
         padding: 1rem;
         display: flex;
         justify-content: space-around;
         background-color: $white;

         .logo{
            
             img{
                width: 3.5rem;
             }
         }
         .list{
            display: flex;
            list-style: none;
            gap: 1rem;
            margin: 1rem;

                 a{
                   text-decoration: none;
                   color: $black;
                   font-size: .6rem;
                 }
                     &:hover{
                        background-color: $blue;
                     }
        }


         
         
   }

</style>