<template>
    <div v-if="5 >= 5" class="rating">
        2.9/5
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
    </div>
    <div v-else-if="5 >= 4" class="rating">
        2.9/5
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
    </div>
    <div v-else-if="5 >= 3" class="rating">
        2.9/5
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
    </div>
    <div v-else-if="5 >= 2" class="rating">
        2.9/5
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
    </div>
    <div v-else-if="5 >= 1" class="rating">
        2.9/5
        <div :class="{ circleWoman: true, circleMan: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
    </div>
    <div v-else class="rating">
        2.9/5
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
        <div :class="{ circle2Woman: true, circle2Man: false }"></div>
    </div>
</template>
<script>
export default {
    name: "RatingComponent",
    props: ['colorPallette']
};
</script>
<style scoped>
.circleWoman {
    height: 18px;
    width: 18px;
    border: 2px solid #720060;
    background-color: #720060;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}

.circle2Woman {
    height: 18px;
    width: 18px;
    border: 2px solid #720060;
    background-color: white;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}

.circleMan {
    height: 18px;
    width: 18px;
    border: 2px solid #002772;
    background-color: #002772;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}

.circle2Man {
    height: 18px;
    width: 18px;
    border: 2px solid #002772;
    background-color: white;
    border-radius: 50%;
    display: inline-block;
    margin-left: 5px;
}
</style>
