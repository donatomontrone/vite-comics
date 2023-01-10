<template>
    <main>
        <div class="wrapper">
            <section class="main-content">
                <h3> --> Content goes here </h3>
            </section>
        </div>
        <section class="banner">
            <div class="wrapper">
                <ul>
                    <li v-for="item in blueButtonsList">
                        <img :src="getImagePath(item.img)" :alt="item.text">
                        <p>{{ item.text.toUpperCase() }}</p>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>
<script>
export default {
    data() {
        return {
            blueButtonsList: [
                {
                    text: 'digital comics',
                    img: "comics-digital-comics.png"
                },
                {
                    text: 'dc merchandise',
                    img: "comics-merchandise.png"
                },
                {
                    text: 'subscription',
                    img: "comics-subscriptions.png"
                },
                {
                    text: 'comic shop locator',
                    img: 'comics-shop-locator.png'
                },
                {
                    text: 'dc power visa',
                    img: "dc-power-visa.svg"
                }
            ],
        }
    },
    methods: {
        getImagePath: function (img) {
            return new URL((`../assets/img/buy-${img}`), import.meta.url).href;
        }
    }

}
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

h3 {
    color: $light-color;
    padding: 2.5rem 0;
}

section.banner {
    background-color: $main-color;

    ul {
        list-style: none;
        display: flex;
        justify-content: space-around;
        height: 100%;
        color: $light-color;

        li {
            display: flex;
            padding: 1.5rem;
            font-size: .8rem;
            align-items: center;

            img {
                width: 44px;
                aspect-ratio: 3/2;
                object-fit: contain;
                mix-blend-mode: normal;
                margin-right: .5rem;

            }
        }
    }
}
</style>