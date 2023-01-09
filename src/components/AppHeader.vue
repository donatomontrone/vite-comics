<template>
    <div class="container">
        <div class="wrapper">
            <div class="main-logo">
                <img src="../assets/img/dc-logo.png" alt="DC Comics Main Logo">
            </div>
            <nav>
                <ul>
                    <li v-for="item in navItems" :class="(item.active) ? 'active' : ''">{{ item.text.toUpperCase() }}
                    </li>
                </ul>
            </nav>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {
            navItems: [
                {
                    text: 'characters',
                    active: false
                },
                {
                    text: 'comics',
                    active: true
                },
                {
                    text: 'movies',
                    active: false
                },
                {
                    text: 'tv',
                    active: false
                },
                {
                    text: 'games',
                    active: false
                },
                {
                    text: 'collectibles',
                    active: false
                },
                {
                    text: 'videos',
                    active: false
                },
                {
                    text: 'fans',
                    active: false
                },
                {
                    text: 'news',
                    active: false
                },
                {
                    text: 'shop',
                    active: false
                }
            ]
        }
    }

}
</script>
<style lang="scss" scoped>
div.container {
    margin-top: 4rem;
    background-color: white;

    div.wrapper {
        display: flex;
        justify-content: space-between;
        align-items: center;
    }

    div.main-logo img {
        width: 60px;
        padding: .8rem 0;
    }

    ul {
        list-style-type: none;

        li {
            display: inline;
            padding: 2.1rem 0;
            margin: 0 .7rem;
            font-size: .65rem;
            font-weight: bold;

            &.active {
                color: #267CEC;
                border-bottom: 4px solid #267CEC;
            }
        }
    }
}
</style>