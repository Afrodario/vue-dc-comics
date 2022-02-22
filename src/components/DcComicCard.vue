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
    .comic-card {
        height: 100px;
        width: 100px;
        flex-direction: column;
        margin: 10px;

        img {
            width: 100%;
            height: 100%;
            object-fit: cover;
        }

        .comic-title {
            font-size: 10px;
        }
    }
</style>