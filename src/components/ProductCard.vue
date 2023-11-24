<script>
export default {
    props: {
        title: String,
        image: String,

    },

}
</script>

<template>
    <div class="card">
        <img :src="image" alt="">
       
        <h3>{{ title }}</h3>

    </div>

</template>

<style scoped lang="scss">
@use "../style/partials/variables" as *;
.card{
    height: 100%;
    

    img{
        max-height: 100px;
        width: 100%;
        object-fit: cover;
      
    }
};

h3{
    color: $white;
    font-size: .8rem;
}

</style>