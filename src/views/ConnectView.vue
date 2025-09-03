<script setup>
import HeaderComponent from '../components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import { ref } from 'vue';
const icons = ref([
    {
        id: 1,
        name: "instagram",
        nameCap: "Instagram",
    },
    {
        id: 2,
        name: "behance",
        nameCap: "Behance",
    },
    {
        id: 3,
        name: "dribbble",
        nameCap: "Dribbble",
    },
    {
        id: 4,
        name: "linkedin",
        nameCap: "LinkedIn",
    },

])
</script>

<template>
    <HeaderComponent />
    <main>
        <section class="banner">

            <h1><span>Connect</span></h1>

            <p>
                I’m always open to new opportunities and collaborations. Whether you’re looking to start a project or
                just want to chat, feel free to reach out.
            </p>
        </section>

        <section class="connect">
            <ul class="white-itens">
                <li v-for="brand in icons">
                    <a href="#"><span :class="'fa-brands fa-' + brand.name"></span>{{ brand.nameCap }}</a>
                </li>
            </ul>
        </section>
    </main>
    <FooterComponent />
</template>

<style scoped>
section.connect {
    & ul {
        & li {
            text-align: center;

            & span {
                font-weight: bold;
                padding: 0 15px 0 0;
            }
        }
    }
}
</style>
