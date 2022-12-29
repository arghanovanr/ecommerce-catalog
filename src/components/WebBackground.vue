<template >
    <div :class="{ BackgroundWoman: false, BackgroundMan: true }">

    </div>
</template>
<script>
export default {
    name: "WebBackgorund"
}
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
    background-color: #D6E6FF;
    background-image: url("../assets/bg-pattern.svg");
}
</style>