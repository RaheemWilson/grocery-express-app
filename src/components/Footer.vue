<template>
  <footer>
      <div class="footer">
         <div class="logo links">
             <div class="footer-logo">
              <img src="@/assets/logo.svg" alt="App logo"/>
              <h4 class="name">Grocery Express</h4>
            </div>
            <p class="info">
                Fast delivery, which is active all over the world, serves with many transportation vehicles.</p>
         </div>
         <div class="links">
            <p class="title">Company</p>
            <ul>
                <li>About Us</li>
                <li>Blog</li>
                <li>All Products</li>
                <li>Locations Map</li>
            </ul>
         </div>
         <div class="links">
            <p class="title">Services</p>
            <ul>
                <li>Order tracking</li>
                <li>Wish List</li>
                <li>My account</li>
                <li>{{"Terms & Condition"}}</li>
            </ul>
         </div>
         <div class="links">
            <p class="title">Get in touch</p>
            <p class="info">
                Subscribe to our weekly newsletter and receive updates via email.
            </p>
         </div>
      </div>
      <hr/>
    <div class="rights-reserved">
        <p>All Rights Reserved @Raheem Wilson 2021</p>
        <div>
            <p>{{"Terms & Conditions"}}</p>
            <p>{{"Privacy & Policy"}}</p>
        </div>
    </div>
  </footer>
</template>

<script>
export default {
 name: "Footer",
 
}
</script>


<style lang="scss" scoped>
@import "@/scss/_variables.scss";

footer{
    padding: 3rem 7rem 1rem 7rem;

    @media only screen and (max-width: 900px){
        padding: 2rem;
    }
}

.footer{
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    gap: 8rem;
    padding-bottom: 1rem;
    font-size: 16px;

    @media only screen and (max-width: 900px){
        grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
        gap: 2rem;
    }
    
    @media only screen and (max-width: 600px){
        gap: 1rem;
    }

    .links{
        display: grid;
        grid-template-rows: 1fr 2fr;
        align-items: flex-start;

        
    }

    .logo{
        @media only screen and (max-width: 600px){
            grid-template-rows: 1fr 1fr;
        }
    }

    .title{
        font-weight: 600;
    }

    .footer-logo{
        display: flex;
        align-items: center;
        gap: 0.5rem;

        img{
            width: 2rem;
            height: 2rem;
        }
    }

    .info, ul{
        color: #676767;
    }

    .info{
        margin: 0;
    }

    ul{
        list-style: none;
        padding: 0;
        margin: 0;

        li{
            margin-bottom: 10px;
        }
    }

}

.rights-reserved{
    display: flex;
    justify-content: space-between;
    flex-wrap: wrap;
    color: #676767;
    font-size: 14px;

    div{
        display: flex;
        gap: 1rem;
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
