<template>
  <header>
      <div class="header">
          <div class="header-logo">
              <img src="@/assets/logo.svg" alt="App logo"/>
              <h2 class="header-name">Grocery Express</h2>
          </div>
          <MobileMenu v-if="mobile"></MobileMenu>
          <div class="nav-responsive" v-else>
            <nav class="header-nav">
                <ul class="nav-menu">
                    <li class="nav-item"><router-link to="/">Home</router-link></li>
                    <li class="nav-item"><router-link to="/about">About</router-link></li>
                    <li class="nav-item"><router-link to="/services">Services</router-link></li>
                    <li class="nav-item"><router-link to="/contact">Contact Us</router-link></li>
                </ul>
            </nav>
        </div>
          
      </div>
  </header>
</template>

<script>
import MobileMenu from '@/components/MobileMenu.vue'
export default {
    name: "Header",
    components: {
        MobileMenu
    },
    data(){
        return{
            mobile: false,
        }
    },

    mounted() {
        this.onResize()
        window.addEventListener('resize', this.onResize, { passive: true });
    },

    methods: {  
        onResize() {
           this.mobile = window.innerWidth < 1200
        },
    }
 
}
</script>


<style lang="scss" scoped>
@import "@/scss/_variables.scss";
header{
    padding: 0 7rem;
    background-color: #ffffff;
	position: -webkit-sticky;
	position: sticky;
	top: 0;
    z-index: 1;

    @media (max-width: 1024px){
        padding: 0 1rem;
    }

    
}

.header{
    display: flex;
    justify-content: space-between;
    align-items: center;

    :last-child(){
        justify-content: right;
    }

    .header-logo{
        display: flex;
        align-items: center;

        img{
            width: 2.5em;
            height: 2.5em;
            padding-right: 1rem;
            @media only screen and (max-width: 400px){
                width: 2em;
                height: 2em;
                padding-right: 0.5rem;
            }
        }

        h2{
            color: $red;
            @media only screen and (max-width: 400px){
                font-size: 1.5rem;
            }
        }
    }

    .header-nav{
        display: flex;
        justify-content: center;
       

        .nav-menu {
            display: flex;
            gap: 1rem;
            padding: 0;
            margin: 0;
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
}
.hamburger-menu{
    width: 3rem;
    height: 3rem;
    display: flex;
    align-items: center;
    justify-content: center;
}

.nav-item{
    a {
        padding: 0.75rem 0.25rem;
        text-decoration: none;
        color: $black;
    }

    a.router-link-active{
        color: $red;
        border-bottom: 3px solid $red;
    }
}
</style>
