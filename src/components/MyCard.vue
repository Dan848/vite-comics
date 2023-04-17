<template>
    <div class="col-12 col-sm-6 col-md-3 col-lg-2 d-flex flex-column align-items-center justify-content-center">
        <div class="img-box d-flex justify-content-center"><img class="img-fluid" :src="image" :alt="title"></div>
        <div class="text-center">{{ title }}</div>
    </div>
</template>

<script>
    export default {
        name: "MyCard",
        props: {
        image: String,
        title: String,
        }
    }
</script>

<style lang="scss" scoped>
    .img-box {
        max-width: 150px;

        img{
        width: 150px;
        height: 150px;
        object-fit: cover;
        object-position: top;
        }

    }


</style>