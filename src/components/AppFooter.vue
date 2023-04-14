<template>
    <footer>
        <div class="footer-top p-5">
            <div class="container">
                <div class="row">
                    <div v-for="(list, index) in footerUl" :key="index" class="col">
                        <h4 class="text-white text-uppercase">{{ list.title }}</h4>
                        <ul class="list-unstyled">
                            <li v-for="(link, ind) in list.links" :key="ind">
                                <a class="opacity-50 text-capitalize" :href="link.href">{{ link.text }}</a>
                            </li>
                        </ul>
                    </div>
                    <div class="col">
                        
                    </div>
                </div>
            </div>
        </div>
        <div class="footer-bottom">
            <div class="container d-flex align-items-center justify-content-between py-4">
                <div><button class="text-uppercase text-white px-3 py-2">sign-up-now!</button></div>
                <div class="d-flex align-items-center">
                    <h5 class="text-uppercase dc-text-primary my-0">follow us</h5>
                    <div class="ms-4">
                        <img class="ms-3" src="/img/footer-facebook.png" alt="Our Facebook Page">
                        <img class="ms-3" src="/img/footer-twitter.png" alt="Our Twitter Page">
                        <img class="ms-3" src="/img/footer-youtube.png" alt="Our Youtube Page">
                        <img class="ms-3" src="/img/footer-pinterest.png" alt="Our Pinterest Page">
                        <img class="ms-3" src="/img/footer-periscope.png" alt="Our Periscope Page">
                    </div>
                </div>
            </div>
        </div>
    </footer>
</template>

<script>
import  {footerLinks} from "../data/data.js"
    export default {
        name: "AppFooter",
        data() {
            return {
                footerUl: footerLinks,
            }
        },
        methods : {
        }
    }
</script>

<style lang="scss" scoped>
    @use "../assets/styles/var.scss" as *;
    .footer-top{
        background: url("./img/footer-bg.jpg");
        background-repeat: no-repeat;
        background-size: cover;
        
        a {
            text-decoration: none;
            color: white;
        }
    }
    .footer-bottom{
        background: $dc-bg-footer;
        button {
            border: 2px solid $dc-primary;
            background-color: $dc-bg-footer;
            font-weight: 600;
        }
    }
</style>