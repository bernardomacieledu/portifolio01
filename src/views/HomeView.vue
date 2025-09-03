<script setup>
import HeaderComponent from '../components/HeaderComponent.vue'
import FooterComponent from '../components/FooterComponent.vue'
import { ref } from 'vue';

const cartoes = ref([
    {
        id: 1,
        title: "ShopEase",
        description: null,
        image: "shopease.png",
        emoji: null,
        categorias: [
            "Mobile", "Application", "E-commerce"],
    },
    {
        id: 2,
        title: "Insightly",
        image: null,
        emoji: "💡",
        description: "Developed a SaaS-based analytics dashboard for Insightly, focusing on providing actionable insights through a user-centric design. The dashboard improved data accessibility and was adopted by 80% of users within the first three months.",
        categorias: [
            "Web 3.0", "HTML", "Dashboard"],
    },
    {
        id: 3,
        title: "ShopEase",
        description: null,
        image: "shopease.png",
        emoji: null,
        categorias: [
            "Mobile", "Application", "E-commerce"],
    },
    {
        id: 4,
        title: "Insightly",
        image: null,
        emoji: "💡",
        description: "Developed a SaaS-based analytics dashboard for Insightly, focusing on providing actionable insights through a user-centric design. The dashboard improved data accessibility and was adopted by 80% of users within the first three months.",
        categorias: [
            "Web 3.0", "HTML", "Dashboard"],
    },
]);

</script>

<template>

    <HeaderComponent />
    <main>
        <section class="banner">

            <h1>Hi, I’m <span>Alex</span></h1>

            <p>
                a <strong>UI/UX Designer</strong> based in <strong>Los Angeles</strong>. With over <strong>3 years of
                    experience</strong>, I specialize in creating
                user-friendly digital products that solve real-world problems.
            </p>
        </section>

        <section class="cards">
            <ul>
                <li v-for="card in cartoes">
                    <h3>{{ card.title }}</h3>
                    <p v-if="card.image != null">
                        <img :src="'/images/' + card.image" :alt="card.image">
                    </p>
                    <div v-if="card.emoji != null">
                        <p class="emogi">{{ card.emoji }}</p>
                        <p>{{ card.description }}</p>
                    </div>
                    <ul>
                        <li v-for="cat in card.categorias">{{ cat }}</li>
                    </ul>
                </li>
            </ul>
        </section>
    </main>
    <FooterComponent />shopease.png
    Insightly

    💡

    Developed a SaaS-bas

</template>

<style scoped>
section.cards>ul {

    &>li {
        background: white;
        border-radius: 10px;
        padding: 20px;
        margin-bottom: 20px;

        & h3 {
            font-size: 1.5rem;
        }

        & img {
            border-radius: 10px;
        }

        & .emogi {
            font-size: 4rem;
        }
    }

    & ul {
        display: flex;
        margin-top: 20px;

        & li:first-child {
            margin-left: 0;
        }

        & li {
            background: rgb(232, 232, 232);
            color: black;
            margin: 0 10px;
            padding: 4px 8px;
            border-radius: 10px;
            font-size: 0.7rem;
            font-weight: bold;
        }
    }
}
</style>
