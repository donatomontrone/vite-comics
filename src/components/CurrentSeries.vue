<template>
    <div class="card">
        <img :src="path" :alt="series">
        <p>{{ series }} </p>
    </div>
</template>
<script>

export default {
    name: "CurrentSeries",
    props: {
        path: String,
        price: String,
        series: String,
        type: String
    }
}
</script>
<style lang="scss">
@use '../styles/partials/variables.scss' as *;

div.card {
    width: calc(100% / 6 - 2rem);
    margin: .5rem 1rem;

    p {
        text-align: center;
        text-transform: uppercase;
        color: $light-color;
        font-weight: lighter;
    }
}
</style>