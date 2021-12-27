<template>
  <div class="main">
    <div class="hero-container">
      <div class="hero-content">
        <div class="hero-ad">
          <p>More than Faster</p>
          <img src="@/assets/strawberry-image.svg" alt="image"/>
        </div>
        <h1 class="hero-title">Groceries delivered in as little as <span>2 hours</span></h1>
        <p class="hero-info">Grocen atssures fresh grocery every morning to your family without getting out in this pandemic.</p>
        <div class="buttons">
          <div class="cta">Order Now</div>
          <div class="order-process">
            <div class="order-process-btn">
              <img src="@/assets/triangle.svg" alt="image"/>
            </div>
            <p>Order Process</p>
          </div>
        </div>
      </div>
      <div class="hero-image">
        <img src="@/assets/HeaderImage.png" alt="Hero image">
      </div>
    </div>
    <div class="what-we-serve-container">
      <div class="what-we-serve-content">
        <div class="title">
          <p>What we serve</p>
          <h1>Fruit And Vegetable Delivered To Your Home</h1>
        </div>
        <div class="cards">
          <div class="card">
            <div class="card-content">
              <img class="card-icon" src="@/assets/delivery-icon.svg" alt="icon">
              <p class="card-title">Free shipping</p>
              <p class="card-desc">Enjoy order in a hand using the freshness of groceries</p>
            </div>
          </div>
          <div class="card">
            <div class="card-content card-down">
              <img class="card-icon" src="@/assets/returns-icon.svg" alt="icon">
              <p class="card-title">5 days return</p>
              <p class="card-desc">If you get rotten items - return immediately to us.</p>
            </div>
          </div>
          <div class="card">
            <div class="card-content">
              <img class="card-icon" src="@/assets/secure-icon.svg" alt="icon">
              <p class="card-title">Secure checkout</p>
              <p class="card-desc">Pay for your fruits and vegetables without a hassle.</p>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="why-choose-us-container">
      <div class="why-choose-us-content">
          <div class="content-info">
            <div class="title">
              <p>Why choose us</p>
              <h1>Find Favorites And Discover New Ones</h1>
            </div>
            <p class="info">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. 
              Aut eos, illo commodi quisquam est vero voluptatibus molestias atque? Assumenda, quaerat?
            </p>
            <button class="explore-now-btn">Explore Now</button>
          </div>
        <div class="content-image">
          <img src="@/assets/discover.svg" alt="Discover photo" class="main-img"/>
        </div>
      </div>
    </div>
    <div class="home-delivery-container">
      <div class="home-delivery-content">
          <div class="content-info">
            <div class="title">
              <p>Home delivery</p>
              <h1>Sit at Home We Will Take Care Your Order</h1>
            </div>
            <p class="info">
              Lorem ipsum dolor sit amet consectetur adipisicing elit. 
              Aut eos, illo commodi quisquam est vero voluptatibus molestias atque? Assumenda, quaerat?
            </p>
            <button class="explore-now-btn">Explore Now</button>
          </div>
        <div class="content-image">
          <img src="@/assets/chef.svg" alt="Discover photo" class="main-img"/>
        </div>
      </div>
    </div>
    <div class="sign-up-container">
      <div class="sign-up-content">
        <div class="content-info">
          <div class="title">
            <p>Download our app</p>
            <h1>Get The Groceries App Order More Easily.</h1>
          </div>
          <p class="info">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, laboriosam! Suscipit commodi similique ullam minus.
          </p>
          <div class="badges">
            <a href="https://play.google.com/store/apps/">
              <img src="@/assets/google-play-badge.png" alt="App store">
            </a>
            <a href="https://www.apple.com/lae/app-store/">
              <img src="@/assets/app-store-badge.png" alt="App Store">
            </a>
          </div>
        </div>
        <div class="content-image">
          <img src="@/assets/mockup.svg" alt="Discover photo" class="main-img"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>

export default {
  name: 'Home',
}
</script>

<style lang="scss" scoped>

.hero-container,
.what-we-serve-container, 
.why-choose-us-container, 
.home-delivery-container,
.sign-up-container{
  display: flex;
  align-items: center;
  justify-content: center;
  margin-top: 4rem;
  padding: $padding;
  background: $light-red;
  max-width: 100%;

  @media only screen and (max-width: 1000px){
    margin-top: 2rem;
    padding: 1rem;
    flex-wrap: wrap-reverse;
  }
  
}

.hero-container{
  background: #fff;
  .hero-content{
    @media only screen and (max-width: 1200px){
      margin-top: 2rem;
    }

    @media only screen and (max-width: 600px){
      display: flex;
      flex-wrap: wrap;
      justify-content: center;
      text-align: center;
    }
    .hero-ad{
      display: flex;
      justify-content: center;
      align-items: center;
      background: $light-red;
      gap: 10px;
      width: 14rem;
      border-radius: 28px;
      color: $red;

      img{
        box-shadow: 0px 12px 20px rgba(224, 25, 35, 0.2);
      }
    }

    .hero-title{
      font-size: 74px;
      @media only screen and (max-width: 1200px){
        font-size: 46px;
      }
    }

    .hero-info{
      font-size: 18px;
      width: 80%;

      @media only screen and (max-width: 600px){
        width: 100%;
      }
    }

    .buttons{
      display: flex;
      align-items: center;
      margin: 2rem 0;

      .cta{
        height: 3.5rem;
        width: 12rem;
        border-radius: 12px;
        background: $red;
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        font-weight: $medium;
        font-size: 1.25rem;
        @media only screen and (max-width: 600px){
          height: 3rem;
          width: 10rem;
          font-size: 1rem;
        }
      }

      .order-process{
        display: flex;
        align-items: center;
        margin-left: 2rem ;

        .order-process-btn{
          width: 3.5rem;
          height: 3.5rem;
          border-radius: 50%;
          box-shadow: 0px 20px 49px -10px rgba(0, 0, 0, 0.08);
          display: flex;
          justify-content: center;
          align-items: center;
          @media only screen and (max-width: 600px){
            height: 3.8rem;
            width: 3.8rem;
          }
        }

        p{
          font-size: 20px;
          padding-left: 1rem;

          @media only screen and (max-width: 500px){
            display: none;
          }
        }
      }
    }

  }
  .hero-image{
    img{
      width: 40vw;
      height: 34vw;
      @media only screen and (max-width: 1024px){
        width: 80vw;
        height: 70vw;
      }
    }
  }
}

.title{
  display: flex;
  flex-direction: column;
  text-align: center;
  width: 100%;

  
  @media only screen and (min-width: 1024px){
    margin: 0 auto;
    width: 70%;
  }

  p, h1{
    margin: 0;

    @media only screen and (max-width: 1200px){
      text-align: center;
    }
  }

  p{
    font-size: 18px;
    color: $red;
  }

  h1{
    font-size: 40px;

    @media only screen and (max-width: 600px){
      font-size: 24px;
    }
  }
}

.what-we-serve-content{
  padding: 2rem 0;
  .cards{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
    gap: 3rem;
    margin: 4rem 0;

    @media only screen and (max-width: 600px){
      gap: 1rem;
    }


    .card{
      display: flex;
      align-items: center;
      justify-content: center;
    }

    .card-content{
      width: 13rem;
      height: 14rem;
      padding: 2rem;
      display: grid;
      grid-template-rows: 6rem 3rem 1fr;
      justify-content: center;
      align-items: center;
      text-align: center;
      background: #fff;
      border-radius: 12px;

      p{
        margin: 0;
      }

      .card-icon{
        margin: 30px auto;
        filter: drop-shadow(0px 25px 30px rgba(248, 67, 68, 0.1));
      }

      .card-title{
        font-weight: 600;
        font-size: 1.4rem;
        margin-top: 2rem ;
      }

      .card-desc{
        font-size: 14px;
      }
      
    }

    .card-down{
      @media only screen and (min-width: 1200px){
        width: 15rem;
        height: 16rem;
      }
      
    }
  }
}

.why-choose-us-container,
.home-delivery-container,
.sign-up-container{
  background: #fff;
  max-width: 100%;

  .why-choose-us-content,
  .home-delivery-content,
  .sign-up-content{
    display: flex;
    align-items: center;
    flex-direction: row-reverse;
    gap: 2rem;

    @media only screen and (max-width: 1200px){
      justify-content: center;
      flex-wrap: wrap-reverse;
    }

    .content-image{
      position: relative;

      .main-img{
        width: 34.5rem;
        height: 41rem;

        @media only screen and (max-width: 1024px){
          width: 80vw;
          height: 95vw;
        }
      }


    }

    .content-info{
      padding-left: 3rem;

      @media only screen and (max-width: 1200px){
        padding: 0;
      }
      .title{
        margin: 0;
        text-align: left;
        width: 100%;
        p{
          color: #03A66B;
        }
        h1{
          width: 100%;
        }
      }

      .info{
        font-size: 18px;
        width: 80%;

        @media only screen and (max-width: 1200px){
          width: 100%;
          text-align: center;
        }
      }

      .explore-now-btn{
        border: none;
        border-radius: 8px;
        background: $red;
        color: #fff;
        font-size: 1rem;
        font-weight: $medium;
        width: 10rem;
        height: 3rem;
        margin-top: 1.5rem;

        @media only screen and (max-width: 1200px){
          display: block;
          margin: 0 auto;
        }
      }
    }
  }
}

.home-delivery-container{
  .home-delivery-content{
    flex-direction: row;
    .content-info{
      padding: 0;
      .title{
        p{
          color: #F9BA45;
        }
      }

      .explore-now-btn{
        border: 1px solid $red;
        border-radius: 8px;
        background: none;
        color: $red;
      }
    }
  }
}
.sign-up-container{
  background: $light-red;
  padding: 0 7rem;
  .sign-up-content{

    .content-image{
      .main-img{
        height: auto;
        filter: drop-shadow(0px 16px 40px rgba(255, 94, 95, 0.12));
      }
    }
    .content-info{
      .title{
        p{
          color: $red;
        }
      }

      .badges{
        display: flex;
        gap: 1rem;

        @media only screen and (max-width: 1200px){
          justify-content: center;
        }
      }
    }
  }
}
</style>