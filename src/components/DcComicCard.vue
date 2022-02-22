<template>
    <div class="comic-card flex">
        <img :src="thumb" :alt="series">
        <h3 class="comic-title">{{series}}</h3>
    </div>
</template>

<script>
export default {
    name: "DcComicCard",
    props: {
        "thumb": String,
        "series": String
    }
}
</script>

<style scoped lang="scss">
@import "../assets/style/variables.scss";
    .comic-card {
        height: 150px;
        width: 100px;
        flex-direction: column;
        margin: 15px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .comic-title {
            font-size: 10px;
            text-align: center;
            margin: 5px;
            color: white;
        }
    }
</style>