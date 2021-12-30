<template>
    <div class="hamburger-menu"  @click="handleClick">
        <img :src="require(`@/assets/${image}.svg`)" alt="Menu bar"/>
    </div>
     <transition name="slide-fade">
        <div class="nav-responsive" v-if="displayMenu">
            <nav class="header-nav">
                <ul class="nav-menu">
                    <li class="nav-item"><router-link to="/" @click="handleClick">Home</router-link></li>
                    <li class="nav-item"><router-link to="/about" @click="handleClick">About</router-link></li>
                    <li class="nav-item"><router-link to="/services" @click="handleClick">Services</router-link></li>
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
    top: 4rem;
    left: 0;
    right: 0;
    :not(:first-child){
        display: flex;
        align-items: center;
        flex-direction: column;
    }
}

.clear-btn{
    display: flex;
    justify-content: right;
    margin-bottom: 1rem;
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