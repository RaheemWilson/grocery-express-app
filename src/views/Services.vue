<template>
    <div class="services-container">
        <h1 class="services-title" data-aos="zoom-in" data-aos-duration="800">Our Services</h1>
        <div class="services-content">
            <div class="service">
                <img src="@/assets/farming.jpg" alt="Farming" data-aos="fade-right" data-aos-duration="800">
                <div data-aos="fade-left" data-aos-duration="800">
                    <h2>We produce organic fruits and vegetables</h2>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Modi ipsa tempore corrupti quae ut aliquam deleniti beatae molestiae cum consequuntur!
                    </p>
                </div>
            </div>
            <div class="service">
                <div data-aos="fade-left" data-aos-duration="800">
                    <h2>We do fast delivery</h2>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Modi ipsa tempore corrupti quae ut aliquam deleniti beatae molestiae cum consequuntur!
                    </p>
                </div>
                <img src="@/assets/delivery.jpg" alt="Delivery" data-aos="fade-right" data-aos-duration="800">
            </div>
            <div class="service">
                <img src="@/assets/payment.jpg" alt="Payment" data-aos="fade-right" data-aos-duration="800">
                <div data-aos="fade-left" data-aos-duration="800">
                    <h2>We provide secured payment options</h2>
                    <p>Lorem ipsum dolor sit, amet consectetur adipisicing elit. 
                        Modi ipsa tempore corrupti quae ut aliquam deleniti beatae molestiae cum consequuntur!
                    </p>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: "Services",
}
</script>

<style lang="scss" scoped>
.services-container{
    padding: $padding;
    max-width: 100%;

    @media only screen and (max-width: 1000px){
        margin-top: 2rem;
        padding: 1rem;
    }
}

.service{
    display: flex;
    align-items: center;
    gap: 1rem 3rem;
    margin: 2rem 0;
    transform: translate(0px, 0px);
    opacity: 1;
    @media only screen and (max-width: 1100px){
        flex-wrap: wrap;
        justify-content: center;
        text-align: center;
    }

    &:nth-child(2){
        @media only screen and (max-width: 1100px){
            flex-wrap: wrap-reverse;
        }
    }
    img{
        width: 35rem;
        box-shadow: 0px 16px 40px -25px rgba(0, 0, 0, 0.08);
        @media only screen and (max-width: 700px){
            width: 80vw;
        }
    }

    div{
        padding-left: 1rem;
        border-left: 4px solid $red;
        @media only screen and (max-width: 1100px){
            border-left: none;
            padding-left: 0 ;
            width: 60vw;
        }
    }



}

.services-title{
    font-size: 74px;
    text-align: left;
    color: $red;
    @media only screen and (max-width: 1100px){
        font-size: 46px;
        text-align: center;
    }
}
</style>