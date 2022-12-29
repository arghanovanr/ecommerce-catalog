<template>
    <div :class="{ customButtonWoman: woman, customButtonMan: man }">
        <button>NEXT PRODUCT</button>
    </div>
</template>

<script>
export default {
    name: "NextProductButton",
    props: ["woman", "man"],
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
</style>
