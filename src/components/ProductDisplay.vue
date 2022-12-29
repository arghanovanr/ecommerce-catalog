<template>
    <div v-if="!data.unavaliable" class="view">
        <div class="card">
            <div class="imageBox">
                <img :src="data.image" />
            </div>
            <div class="textContainer">
                <div class="headingBox">
                    <div :class="{ colorPalletteWoman: data.woman, colorPalletteMan: data.man, }">
                        {{ data.productName }}
                    </div>
                </div>
                <div class="categoryBox">
                    <div class="container">
                        <div class="category">{{ data.category }}</div>
                        <RatingComponent :woman="data.woman" :man="data.man" :rating="data.rating" />
                    </div>
                </div>
                <div class="descriptionBox">
                    {{ data.description }}
                </div>
                <div class="footerBox">
                    {{ data.price }} <br />
                    <div class="buttonContainer">
                        <div class="buttonItem">
                            <BuyButton :woman="data.woman" :man="data.man" />
                        </div>
                        <div class="buttonItem">
                            <NextProductButton :woman="data.woman" :man="data.man" />
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
    <div v-else class="unavaliableView">
        <div class="unavaliableCard">
            This product is unavaliable to show
            <NextProductButton :unavaliable="data.unavaliable" />
        </div>
    </div>

</template>
<script>
import RatingComponent from "./RatingComponent.vue";
import BuyButton from "./BuyButton.vue";
import NextProductButton from "./NextProductButton.vue";

export default {
    name: "ProductDisplay",
    props: ["dataComponent"],
    components: {
        RatingComponent,
        BuyButton,
        NextProductButton,
    },
    data() {
        return {
            title: "data",
            data: this.dataComponent,
        };
    },
};
</script>
<style scoped>
/* Color Pallette CSS */

.colorPalletteWoman {
    color: #720060;
}

.colorPalletteMan {
    color: #002772;
}

/* Unavaliable View CSS */

.unavaliableView {
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.unavaliableCard {
    box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.2);
    background-color: white;
    width: 82%;
    height: 70%;
    display: flex;
    text-align: center;
    justify-content: center;
    flex-direction: column;
    font-family: "Prompt", sans-serif;
    font-weight: 550;
    font-size: 1.2rem;
    background-image: url("../assets/sad-face.svg");
    background-position: center;
    background-repeat: no-repeat;
}

/* Normal View CSS */

.view {
    width: 100vw;
    height: 100vh;
    display: flex;
    align-items: center;
    justify-content: center;
}

.card {
    box-shadow: 0 4px 10px 0 rgba(0, 0, 0, 0.2);
    background-color: white;
    width: 82%;
    height: 70%;
    display: flex;
}

.imageBox {
    flex: 2;
    display: flex;
    align-items: center;
    justify-content: center;
    box-sizing: border-box;
}

.imageBox img {
    max-width: 80%;
    max-height: 80%;
}

.textContainer {
    flex: 3;
    box-sizing: border-box;
    padding: 15px;
    display: flex;
    flex-direction: column;
}

.headingBox {
    flex: 2;
    font-family: "Prompt", sans-serif;
    font-weight: 550;
    font-size: 2rem;
    line-height: 1.2;
    display: flex;
    align-items: center;
    justify-content: center;
}

.categoryBox {
    flex: 1;
    font-family: "Prompt", sans-serif;
}

.container {
    width: 100%;
    display: flex;
    align-items: flex-end;
    justify-content: space-between;
    padding-bottom: 10px;
    border-bottom: 2px solid rgb(206, 206, 206);
}

.descriptionBox {
    flex: 4;
    font-family: "Prompt", sans-serif;
    line-height: 1.2;
    font-size: 1.2rem;
}

.footerBox {
    border-top: 2px solid rgb(206, 206, 206);
    padding-top: 10px;
    flex: 2;
    font-family: "Prompt", sans-serif;
    font-weight: 575;
    font-size: 1.4em;
}

.buttonContainer {
    display: flex;
}

.buttonItem {
    flex: 1;
}
</style>
