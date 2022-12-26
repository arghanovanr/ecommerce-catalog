<template >
    <div class="view">
        <div class="card">
            <div class="imageBox">
                <img src="https://fakestoreapi.com/img/81XH0e8fefL._AC_UY879_.jpg" />
            </div>
            <div class="textContainer">
                <div class="headingBox">
                    Lock and Love Women's Removable Hooded Faux Leather Moto Biker Jacket
                </div>
                <div class="categoryBox">
                    <div class="container">
                        <div class="category">
                            "women's clothing"
                        </div>
                        <div class="rating">
                            2.9/5
                            <div class="circle"></div>
                            <div class="circle"></div>
                            <div class="circle"></div>
                            <div class="circle2"></div>
                            <div class="circle2"></div>
                        </div>

                    </div>
                    <hr/>
                </div>
                <div class="descriptionBox">
                    100% POLYURETHANE(shell) 100% POLYESTER(lining) 75% POLYESTER 25% COTTON (SWEATER), Faux leather material for style and comfort / 2 pockets of front, 2-For-One Hooded denim style faux leather jacket, Button detail on waist / Detail stitching at sides, HAND WASH ONLY / DO NOT BLEACH / LINE DRY / DO NOT IRON
                </div>
                <div class="footerBox">
                    <hr/>
                    $29,95 <br>
                    <button type="button">BUY NOW</button>
                    <button type="button">NEXT PRODUCT</button>
                </div>
            </div>
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
        width: 82%;
        height: 70%;
        display: flex;
    }
    
    .imageBox
    {
        flex: 2;
        display: flex;
        align-items: center;
        justify-content: center;
        box-sizing: border-box;
        
    }

    .imageBox img
    {
        max-width : 80%;
        max-height: 80%;
    }

    .circle 
    {
        height: 18px;
        width: 18px;
        border: 2px solid #720060;
        background-color: #720060;
        border-radius: 50%;
        display: inline-block;
        margin-left: 5px;
    }

    .circle2 
    {
        height: 18px;
        width: 18px;
        border: 2px solid #720060;
        background-color: white;
        border-radius: 50%;
        display: inline-block;
        margin-left: 5px;
    }

    .textContainer
    {
        flex: 3;
        box-sizing: border-box;
        padding: 15px;
        display: flex;
        flex-direction: column;
    }

    .rating
    {
        display: flex;
        align-items: center;
        justify-content: center;
        
    }

    .headingBox
    {
        flex : 1;
        font-family: 'Prompt', sans-serif;
        font-weight:550;
        font-size: 1.6rem;
        line-height: 1.2;
        color:#720060;
    }

    .categoryBox
    {
        flex : 1;
        font-family: 'Prompt', sans-serif;
     
    }

    .container
    {
        display: flex;
        justify-content: space-between;
        
    }

    .descriptionBox
    {
        flex : 3;
        font-family: 'Prompt', sans-serif;
        line-height: 1.2;
    }

    .footerBox
    {
        flex : 1;
        font-family: 'Prompt', sans-serif;
        color:#720060;
        font-weight: 575;
        font-size: 1.4em;
    }
</style>