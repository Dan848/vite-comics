<template>
    <section class="w-100 py-5 text-white main-div">
        <div class="container">
            <div class="row">
                <div v-for="(icon,index) in iconsBridge" :key="index" class="col mb-3 d-flex justify-content-center align-items-center gap-1">
                    <div><img class="img-fluid" :src="'./img/'+icon.src" :alt="icon.text"></div>
                    <div class="text-uppercase ms-3">{{ icon.text }}</div>
                </div>
            </div>
        </div>
    </section>
</template>

<script>
import  {bridgeSection} from "../data/data.js"
    export default {
        name: "MainBridge",
        data() {
            return {
                iconsBridge: bridgeSection,
            }
        },
        methods : {
        }
    }
</script>

<style lang="scss" scoped>
    @use "../assets/styles/var.scss" as *;
    section {
        background-color: $dc-primary;
        .col{
            &:hover {
                cursor: pointer;
                filter: invert(1);
            }
            img{
            max-width: 60px;
            max-height: 60px;
            }  
        }

    }
</style>