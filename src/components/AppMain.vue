<template>
    <div>
        <div class="hero-section"><img src="/img/jumbotron.jpg" alt="Jumbotron"></div>
        <div class="p-5 text-white container">
            <div class="row">
                <MyCard v-for="(comic, index) in comicsList" :image="comic.thumb" :title="comic.series"/>
            </div>
        </div>
    </div>
</template>

<script>
    import {comics} from "../data/data.js";
    import MyCard from './MyCard.vue';
    export default {
        name: "AppMain",
        components: {
            MyCard
        },
        data() {
            return {
                comicsList: comics
            }
        },
        methods : {
        }
    }
</script>

<style lang="scss" scoped>
    @use "../assets/styles/var.scss" as *;
    .hero-section {
        max-height: 400px;
        overflow: hidden;
        width: 100%;
        img {
            max-height: 400px;
            width: 100%;
            height: 400px;
            object-fit: cover;
            object-position: top;
        }
    }
    div {
        background-color: $dc-bg-main;
    }
</style>