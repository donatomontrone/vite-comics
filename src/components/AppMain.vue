<template>
    <main>
        <div class="jumbotron">
        </div>
        <section class="current-series">
            <div class="wrapper">
                <h4 class="series-title"> CURRENT SERIES </h4>
                <div class="series-cards">
                    <CurrentSeries v-for="item in comicsList" :path="item.thumb" :price="item.price"
                        :series="item.series" :type="item.type" />
                </div>
                <a href="#"> LOAD MORE </a>
            </div>
        </section>
        <section class="banner">
            <div class="wrapper">
                <ul>
                    <li v-for="item in linkList">
                        <img :src="getImagePath(item.img)" :alt="item.text">
                        <p>{{ item.text.toUpperCase() }}</p>
                    </li>
                </ul>
            </div>
        </section>
    </main>
</template>
<script>
import CurrentSeries from './CurrentSeries.vue';

export default {
    name: 'AppMain',
    components: {
        CurrentSeries
    },
    data() {
        return {
            linkList: [
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
            comicsList: [
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
                    "price": "$19.99",
                    "series": "Action Comics",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
                    "price": "$3.99",
                    "series": "American Vampire 1976",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
                    "price": "$16.99",
                    "series": "Aquaman",
                    "type": "graphic novel"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
                    "price": "$2.99",
                    "series": "Batgirl",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$3.99",
                    "series": "Batman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
                    "price": "$2.99",
                    "series": "Batman Beyond",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
                    "price": "$3.99",
                    "series": "Batman/Superman",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
                    "price": "$4.99",
                    "series": "Batman/Superman Annual",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
                    "price": "$5.99",
                    "series": "Batman: The Joker War Zone",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
                    "price": "$6.99",
                    "series": "Batman: Three Jokers",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
                    "price": "$4.99",
                    "series": "Batman: White Knight Presents: Harley Quinn",
                    "type": "comic book"
                },
                {
                    "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
                    "price": "$16.99",
                    "series": "Catwoman",
                    "type": "graphic novel"
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

div.jumbotron {
    background-image: url(../assets/img/jumbotron.jpg);
    background-position: start;
    background-size: cover;
    background-repeat: no-repeat;
    height: 400px;
}

section.current-series {
    position: relative;
    padding-top: 3rem;

    h4.series-title {
        color: $light-color;
        background-color: $main-color;
        width: fit-content;
        font-size: 1.5rem;
        padding: .4rem .8rem;
        position: absolute;
        top: -18px;
    }

    div.series-cards {
        display: flex;
        justify-content: center;
        flex-wrap: wrap;
    }

    a {
        display: block;
        width: fit-content;
        text-decoration: none;
        color: $light-color;
        background-color: $main-color;
        margin: 0 auto;
        padding: .5rem 2.5rem;
        font-size: .8rem;
        font-weight: bold;
        margin-bottom: 1rem;

    }
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