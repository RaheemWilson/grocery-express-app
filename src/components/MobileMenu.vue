<template>
    <div class="hamburger-menu"  @click="handleClick">
        <img :src="require(`@/assets/${image}.svg`)" alt="Menu bar"/>
    </div>
     <transition name="slide-fade">
        <div class="nav-responsive" v-if="displayMenu">
            <div class="search-area">
                    <div class="item-number">0</div>
                <div class="header-search-bar">
                    <div class="input-bar">
                            <img src="@/assets/search-icon.svg" alt="search icon">
                            <input type="search" name="product-search" id="product-search" placeholder="Search"/>
                            <button class="basket">
                                <img src="@/assets/basket.svg" alt="Basket icon">
                            </button>
                    </div>
                </div>
            </div>
            <nav class="header-nav">
                <ul class="nav-menu">
                    <li class="nav-item"><router-link to="/" @click="handleClick">Home</router-link></li>
                    <li class="nav-item"><router-link to="/about" @click="handleClick">About</router-link></li>
                    <li class="nav-item"><router-link to="/shop" @click="handleClick">Shop</router-link></li>
                    <li class="nav-item"><router-link to="/contact" @click="handleClick">Contact Us</router-link></li>
                </ul>
            </nav>
        </div>
    </transition>
</template>

<script>
export default {
    name: 'MobileMenu',
    data(){
        return {
            displayMenu: false,
            image: "menu_black"
        }
        
    },
    methods: {
        handleClick(){
            this.displayMenu = !this.displayMenu
            this.image = this.image === "menu_black" ? "clear_black" : "menu_black"
        }
    }
}
</script>

<style lang="scss" scoped>

.slide-fade-enter-active {
  transition: all .5s ease;
}
.slide-fade-leave-active {
  transition: all .5s ease;
}
.slide-fade-enter { 
  transform: translateY(-50px);
  opacity: 0;
}
.slide-fade-leave-to {
 transform: translateY(-50px);
  opacity: 0; 
}


.header-nav{
    display: flex;
    justify-content: center;
    background: #fff;

    .nav-menu {
        text-align: center;
        padding: 0;
        list-style-type: none;
        font-weight: $medium;
        font-size: 16px;

        .nav-item{
            margin: 1rem 0;
        }
    }
}

.nav-responsive{
    position: absolute;
    background: #fff;
    top: 4.5rem;
    left: 0;
    right: 0;
    // height: 50%;
    padding: 1rem 0;
    :not(:first-child){
        display: flex;
        align-items: center;
        flex-direction: column;
    }
}

.search-area{
    position: relative;
    @media only screen and (min-width: 330px){
        width: min-content;
        margin: 0 auto;
    }
}

.item-number{
    position: absolute;
    top: 0px;
    right: -10px;
    height: 28px;
    width: 28px;
    border-radius: 50%;
    background: $red;
    display: flex;
    align-items: center;
    justify-content: center;
    color: #fff;
    z-index: 2;

    @media only screen and (max-width: 330px){
        right: 4px;
    }
    
}

.clear-btn{
    display: flex;
    justify-content: right;
    margin-bottom: 1rem;
}

.header-search-bar{
    position: relative;
    text-align: right;
    display: flex;
    justify-content: right;
    align-items: center;

    
    
    .input-bar{
        display: flex;
        justify-content: center;
        align-items: center;
        text-align: right;
        width: auto;
        height: 3rem;
        background: #fff;
        box-shadow: 0px 20px 50px rgba(0, 0, 0, 0.04);
        border-radius: $border-radius;
        margin-top: 1rem;
        padding-left: 1rem;

        img{
            width: 18px;
            height: 18px;
            padding: 1px 5px;
        }

        input{
            width: 12rem;
            height: 2rem;
            border: none;

            ::placeholder{
                color: $black;
                font-size: 18px;
                line-height: 5;
            }
        }

        .basket{
            border: none;
            background: none;
            border-left: 1.5px solid #F2F2F2;
            width: 38px;
            height: 38px;
            padding: 20px;
            display: flex;
            justify-content: center;
            align-items: center;

            img{
                width: 24px;
                height: 24px;
            }
        }
    }
    
}

.nav-item{
    a {
        text-decoration: none;
        color: $black;
    }

    a.router-link-active{
        color: $red;
    }
}

</style>