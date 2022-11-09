<script>
export default{
    name: "AppCard",
    props: {
        cardImg: String,
        cardSeries: String,
    }
}
</script>

<template>
    <div class="cards">
        <img :src="cardImg" :alt="cardSeries">
        <h3>{{cardSeries}}</h3>
    </div>

</template>

<style lang="scss" scoped>
.cards{
    width: calc(100% / 6 - 15px);
    padding-top: 1rem;
    img{
        height: 200px;
        width: 100%;
        object-fit: cover;
        object-position: top;
    }
    h3{
        color: white;
        text-align: center;
        margin-top: 1rem;
    }
}
</style>