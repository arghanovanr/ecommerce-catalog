<template >
    <div class="view">
        <div class="card">

        </div>
    </div>
</template>
<script>
export default {
    name:"ProductDisplay"
}
</script>
<style scoped>
    .view
    {
        width: 100vw;
        height: 100vh;
        display: flex;
        align-items: center;
        justify-content: center;
    }

    .card
    {
        box-shadow: 0 4px 10px 0 rgba(0,0,0,0.2);
        background-color: white;
        width: 80%;
        height: 70%;
    }
</style>