<template>
    <section class="blue-buttons">
        <div class="wrapper">
            <ul>
                <li v-for="item in blueButtonsList">
                    <img :src="`src/assets/img/buy-${item.img}`" :alt="item.text">
                    <p>{{ item.text.toUpperCase() }}</p>
                </li>
            </ul>
        </div>
    </section>
    <section class="footer-top">
        <div class="wrapper">
            <nav>
                <ul>
                    <li>
                        <h5>DC COMICS</h5>
                    </li>
                    <li>Charters</li>
                    <li>Comics</li>
                    <li>Movies</li>
                    <li>TV</li>
                    <li>Games</li>
                    <li>Videos</li>
                    <li>News</li>
                    <li>
                        <h5>SHOP</h5>
                    </li>
                    <li>Shop DC</li>
                    <li>Shop DC Collectibles</li>
                </ul>
                <ul>
                    <li>
                        <h5>DC</h5>
                    </li>
                    <li>Term Of Use</li>
                    <li>Privacy Policy (New)</li>
                    <li>Ad Choices</li>
                    <li>Advertising</li>
                    <li>Jobs</li>
                    <li>Subscriptions</li>
                    <li>Talent Workshops</li>
                    <li>CPSC Certificates</li>
                    <li>Ratings</li>
                    <li>Shop Help</li>
                    <li>Contact Us</li>
                </ul>
                <ul>
                    <li>
                        <h5>SITES</h5>
                    </li>
                    <li>DC</li>
                    <li>MAD Magazine</li>
                    <li>DC Kids</li>
                    <li>DC Universe</li>
                    <li>DC Power Visa</li>
                </ul>
            </nav>
            <div class="logo-bg">
                <img src="../assets/img/dc-logo-bg.png" alt="">
            </div>
        </div>
    </section>
    <section class="footer-bottom">
        <div class="wrapper">
            <a href="#">SIGN-UP NOW!</a>
            <div class="socials">
                <h4>FOLLOW US</h4>
                <a href="#" class=""><img src="../assets/img/footer-facebook.png" alt="Facebook"></a>
                <a href="#" class=""><img src="../assets/img/footer-twitter.png" alt="Twitter"></a>
                <a href="#" class=""><img src="../assets/img/footer-youtube.png" alt="YouTube"></a>
                <a href="#" class=""><img src="../assets/img/footer-pinterest.png" alt="Pinterest"></a>
                <a href="#" class=""><img src="../assets/img/footer-periscope.png" alt="Periscope"></a>
            </div>
        </div>
    </section>
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
    }

}
</script>
<style lang="scss" scoped>
section.blue-buttons {
    background-color: #267cec;

    ul {
        list-style: none;
        display: flex;
        height: 100%;
        color: white;

        li {
            display: flex;
            justify-content: space-between;
            padding: 1.5rem;
            font-size: .8rem;
            align-items: center;

            img {
                width: 35px;
                margin-right: .5rem;

            }
        }
    }
}

section.footer-top {
    height: 280px;
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    div.wrapper {
        display: flex;
        justify-content: space-between;
    }


    nav {
        display: flex;

        ul li {
            font-size: .6rem;
            list-style: none;
            margin-right: .7rem;
            padding: .1rem;
            color: grey;


            h5 {
                font-size: .9rem;
                margin: 1.5rem 0 .5rem 0;
                color: white;
            }
        }
    }

    div.logo-bg img {
        width: 370px;
    }
}

section.footer-bottom {
    background-color: #303030;
    position: relative;
    height: 90px;

    div.wrapper {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;

        &>a {
            text-decoration: none;
            color: white;
            font-weight: bold;
            font-size: .8rem;
            padding: .6rem;
            border: 2px solid #267cec
        }

        div.socials {
            display: flex;
            align-items: center;

            h4 {
                color: #267cec;
                padding-right: 1rem;
            }

            img {
                width: 25px;
                margin: 0 .4rem;
            }
        }
    }
}
</style>