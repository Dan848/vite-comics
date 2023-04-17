<template>
    <header class="container d-flex justify-content-between align-items-center fw-bold">
        <div class="py-3">
            <img class="img-fluid" src="/img/dc-logo.png" alt="Logo DC">
        </div>
        <div class="py-3">
            <ul class="list-unstyled d-flex flex-wrap justify-content-center gap-3 m-0 p-0">
                <li @click="makeActive(index)" :class="{'dc-text-primary': link.active}" class="text-uppercase" v-for="(link, index) in navLinks" :key="index">
                    {{ link.text }}
                </li>
            </ul>
        </div>
    </header>
</template>

<script>
import {headerLinks} from '../data/data.js';
export default {
    name: "AppHeader",
    data() {
        return {
            navLinks: headerLinks
        }
    },
    methods : {
        makeActive(index){
            this.navLinks.forEach((link) => link.active = false)
            this.navLinks[index].active = true;
        }
    }
}
</script>

<style lang="scss" scoped>
    @use "../assets/styles/var.scss" as *;
    header{
        img{
            max-width: 80px;
        }
        li {
            &:hover{
                cursor: pointer;
                color: $dc-primary;
            }    
        }
    }
</style>