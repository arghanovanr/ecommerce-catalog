<template>
    <div class="rating">
        2.9/5
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle"></div>
        <div class="circle2"></div>
        <div class="circle2"></div>
    </div>
</template>
<script>
export default {
    name: "RatingComponent",
};
</script>
<style scoped>
.rating {
    display: flex;
    align-items: center;
    justify-content: center;
}

.circle {
    height: 18px;
    width: 18px;
    border: 2px solid #720060;
    background-color: #720060;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}

.circle2 {
    height: 18px;
    width: 18px;
    border: 2px solid #720060;
    background-color: white;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}
</style>
