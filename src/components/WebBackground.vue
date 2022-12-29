<template>
    <div :class="{ BackgroundWoman: data.woman, BackgroundMan: data.man }"></div>
</template>
<script>
export default {
    name: "WebBackgorund",
    props: ["dataComponent"],
    data() {
        return {
            title: "data",
            data: this.dataComponent,
        };
    },
};
</script>
<style scoped>
.BackgroundWoman {
    position: absolute;
    z-index: -1;
    width: 100vw;
    height: 66vh;
    background-color: #fde2ff;
    background-image: url("../assets/bg-pattern.svg");
}

.BackgroundMan {
    position: absolute;
    z-index: -1;
    width: 100vw;
    height: 66vh;
    background-color: #d6e6ff;
    background-image: url("../assets/bg-pattern.svg");
}
</style>
