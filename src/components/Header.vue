<template>
  <header>
      <div class="header">
          <div class="header-logo">
              <img src="@/assets/logo.svg" alt="App logo"/>
              <h2 class="header-name">Grocery Express</h2>
          </div>
          <nav class="header-nav">
              <ul class="nav-menu">
                  <li class="nav-item">Home</li>
                  <li class="nav-item">Menu</li>
                  <li class="nav-item">Service</li>
                  <li class="nav-item">Shop</li>
              </ul>
          </nav>
          <div class="item-number">2</div>
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
  </header>
</template>

<script>
export default {
 name: "Header",
 
}
</script>


<style lang="scss" scoped>
@import "@/scss/_variables.scss";
header{
    padding: $padding;
}

.header{
    display: grid;
    grid-template-columns: repeat(3,1fr);
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

        // h2{
        //     // letter-spacing: 0;
        //     // -webkit-transform: scaleX(1.2);
        //     // transform: scaleX(1.2);
            
        // }
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







#nav a {
  font-weight: bold;
  color: #2c3e50;
}

#nav a.router-link-exact-active {
  color: #42b983;
}
</style>
