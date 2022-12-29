<template >
    <div :class="{ customButtonWoman: false, customButtonMan: true }">
        <button>NEXT PRODUCT</button>
    </div>
</template>
<script>
export default {
    name: "ButButton",
    props: ['colorPallette']
}
</script>
<style scoped >
.customButtonWoman button {
    border: 2px solid #720060;
    background-color: #720060;
    font-family: 'Prompt', sans-serif;
    color: white;
    padding: 10px;
    margin-right: 20px;
    margin-top: 20px;
    width: 90%;
    border-radius: 5px;
}

.customButtonMan button {
    border: 2px solid #002772;
    background-color: #002772;
    font-family: 'Prompt', sans-serif;
    color: white;
    padding: 10px;
    margin-right: 20px;
    margin-top: 20px;
    width: 90%;
    border-radius: 5px;
}
</style>