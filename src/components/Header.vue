<template>
  <header>
      <div class="header">
          <div class="header-logo">
              <img src="@/assets/logo.svg" alt="App logo"/>
              <h2 class="header-name">Grocery Express</h2>
          </div>
          <div v-if="mobile">
              <img src="@/assets/menu_black.svg" alt="Menu bar"/>
          </div>
          <div class="nav-responsive" v-if="!mobile">
            <nav class="header-nav">
                <ul class="nav-menu">
                    <li class="nav-item"><router-link to="/">Home</router-link></li>
                    <li class="nav-item"><router-link to="/about">About</router-link></li>
                    <li class="nav-item"><router-link to="/service">Service</router-link></li>
                    <li class="nav-item"><router-link to="/shop">Shop</router-link></li>
                </ul>
            </nav>
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
          
      </div>
  </header>
</template>

<script>
export default {
 name: "Header",

 data(){
    return{
        windowWidth: window.innerWidth,
        mobile: false
    }
 },
 watch: {
    windowWidth(newWidth) {
        console.log(newWidth)
        this.mobile = newWidth < 1080
        
    }
 },

    mounted() {
        this.$nextTick(() => {
            window.addEventListener('resize', this.onResize);
        })
    },

    beforeUnmount() { 
        window.removeEventListener('resize', this.onResize); 
    },

    methods: {  
        onResize() {
            this.windowWidth = window.innerWidth

        }
    }
 
}
</script>


<style lang="scss" scoped>
@import "@/scss/_variables.scss";
header{
    padding: $padding;
    
    @media (max-width: 1000px){
        padding: 1rem;
    }
}

.header{
    display: grid;
    grid-template-columns: 1fr 3fr;
    align-items: center;
    position: relative;

    :last-child(){
        justify-content: right;
    }

    .header-logo{
        display: flex;
        align-items: center;

        img{
            width: 2.5rem;
            height: 2.5rem;
            padding-right: 1rem;
        }
    }

    .header-nav{
        display: flex;
        justify-content: center;
       

        .nav-menu {
            display: flex;
            gap: 2rem;
            padding: 0;
            list-style-type: none;
            font-weight: $medium;
            font-size: 16px;
        }
    }

    .nav-responsive{
        position: relative;
        display: flex;
        justify-content: right;
        gap: 10rem;
    }

    .item-number{
        position: absolute;
        top: 0px;
        right: 0px;
        height: 28px;
        width: 28px;
        border-radius: 50%;
        background: $red;
        box-shadow: -6px 9px 24px -6px rgba(238, 67, 67, 0.68);
        display: flex;
        align-items: center;
        justify-content: center;
        color: #fff;

    }

    .header-search-bar{
        position: relative;
        text-align: right;
        display: flex;
        justify-content: right;
        align-items: center;
        margin-right: 1rem ;
        
        .input-bar{
            display: flex;
            justify-content: center;
            align-items: center;
            text-align: right;
            width: 20rem;
            height: 3rem;
            box-shadow: 0px 20px 50px rgba(0, 0, 0, 0.04);
            border-radius: $border-radius;

            img{
                width: 18px;
                height: 18px;
                padding: 1px 5px;
            }

            input{
                width: 14rem;
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
                padding: 10px;
                width: 38px;
                height: 38px;
                padding: 0 5px;

                img{
                    width: 24px;
                    height: 24px;
                }
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
