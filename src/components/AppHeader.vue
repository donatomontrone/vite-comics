<template>
    <header>
        <div class="wrapper">
            <nav>
                <div class="main-logo">
                    <img src="../assets/img/dc-logo.png" alt="DC Comics Main Logo">
                </div>
                <ul>
                    <li v-for="item in navItems" :class="(item.active) ? 'active' : ''">{{ item.text.toUpperCase() }}
                    </li>
                </ul>
            </nav>
        </div>
    </header>
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
@use '../styles/partials/variables.scss' as *;

header {
    background-color: $light-color;

    div.main-logo img {
        width: 60px;
        padding: .8rem 0;
    }

    nav {
        display: flex;
        justify-content: space-between;
        align-items: center;
        height: 90px;
    }

    ul {
        list-style-type: none;
        display: flex;
        height: 100%;

        li {
            display: inline-block;
            margin: 0 .7rem;
            font-size: .9rem;
            line-height: 90px;
            font-weight: bold;

            &.active {
                color: $main-color;
                border-bottom: 4px solid $main-color;
            }
        }
    }
}
</style>