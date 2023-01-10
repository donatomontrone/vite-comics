<template>
    <footer>
        <section class="footer-top dc-logo">
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
    </footer>
</template>
<script>
</script>
<style lang="scss" scoped>
@use '../styles/partials/variables.scss' as *;

footer {
    background-color: $footer-bg-color;
    background-image: url(../assets/img/footer-bg.jpg);
    background-position: center top;
    background-repeat: no-repeat;
    background-size: cover;
    position: relative;

    section.dc-logo {
        background-image: url(../assets/img/dc-logo-bg.png);
        background-position: right center;
        background-size: initial;
        background-repeat: no-repeat;
        width: 90%;
        margin-left: 22px;
        padding-bottom: 30px;
    }
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
            color: $light-color;
        }
    }
}

section.footer-bottom {
    background-color: $footer-bg-color;
    height: 90px;

    div.wrapper {
        height: 100%;
        display: flex;
        align-items: center;
        justify-content: space-between;

        &>a {
            text-decoration: none;
            color: $light-color;
            font-weight: bold;
            font-size: .8rem;
            padding: .6rem;
            border: 2px solid $main-color
        }

        div.socials {
            display: flex;
            align-items: center;

            h4 {
                color: $main-color;
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