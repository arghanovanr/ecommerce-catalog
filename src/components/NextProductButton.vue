<template>
    <div :class="{ customButtonWoman: woman, customButtonMan: man, customButton: unavaliable, }">
        <button>NEXT PRODUCT</button>
    </div>
</template>

<script>
export default {
    name: "NextProductButton",
    props: ["woman", "man", "unavaliable"],
};
</script>

<style scoped>
.customButtonWoman button {
    border: 2px solid #720060;
    background-color: white;
    font-family: "Prompt", sans-serif;
    font-weight: 700;
    color: #720060;
    padding: 10px;
    margin-right: 20px;
    margin-top: 20px;
    width: 90%;
    border-radius: 5px;
}

.customButtonMan button {
    border: 2px solid #002772;
    background-color: white;
    font-family: "Prompt", sans-serif;
    font-weight: 700;
    color: #002772;
    padding: 10px;
    margin-right: 20px;
    margin-top: 20px;
    width: 90%;
    border-radius: 5px;
}

.customButton button {
    border: 2px solid black;
    background-color: white;
    font-family: "Prompt", sans-serif;
    font-weight: 700;
    color: black;
    padding: 10px;
    margin-right: 20px;
    margin-top: 20px;
    width: 50%;
    border-radius: 5px;
}
</style>
