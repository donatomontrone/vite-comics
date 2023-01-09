<template>
    <div class="container">
        <div class="wrapper">
            <section class="footer-top">
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
            </section>
        </div>
    </div>
    <section class="footer-bottom">
        <div class="wrapper">
            <a href="#">Cliccami</a>
            <div class="socials">
                <h4>Follow</h4>
                <a href="#" class="">L</a>
                <a href="#" class="">L</a>
                <a href="#" class="">L</a>
                <a href="#" class="">L</a>
            </div>
        </div>
    </section>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
div.container {
    background-image: url(../assets/img/footer-bg.jpg);
    background-repeat: no-repeat;
    background-size: cover;

    section.footer-top {
        display: flex;
        justify-content: space-between;
        height: 230px;


        nav {
            display: flex;

            ul li {
                font-size: .6rem;
                list-style: none;
                margin-right: .7rem;
                color: grey;


                h5 {
                    font-size: .8rem;
                    margin: 1rem 0 .3rem 0;
                    color: white;
                }
            }
        }

        div.logo-bg img {
            width: 280px;
            object-fit: cover;
        }
    }

}

section.footer-bottom {
    background-color: rgb(58, 58, 58);
    position: relative;
}
</style>