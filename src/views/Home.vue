<template>
  <div class="main">
    <div class="hero-content">
      <div class="hero">
        <div class="hero-ad">
          <p>More than Faster</p>
          <img src="@/assets/image.svg" alt="image"/>
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
        <img src="@/assets/hero-image.svg" alt="Hero image">
        <img src="@/assets/pic.svg" alt="card" id="pic-1">
        <img src="@/assets/pic-2.svg" alt="card" id="pic-2">
        <img src="@/assets/abstract.svg" alt="abstract" id="abstract">
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
        <div class="content-image">
          <img src="@/assets/discover.png" alt="Discover photo" class="main-img"/>
          <img src="@/assets/pic-3.svg" alt="Discover card" class="content-card"/>
        </div>
        <!-- <div class="content-container"> -->
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
        <!-- </div> -->
      </div>
    </div>
    <div class="home-delivery-container">
      <div class="home-delivery-content">
        <!-- <div class="content-container"> -->
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
        <!-- </div> -->
        <div class="content-image">
          <img src="@/assets/image-1.svg" alt="Discover photo" class="main-img"/>
        </div>
      </div>
    </div>
    <div class="sign-up-container">
      <div class="sign-up-content">
        <div class="content-image">
          <img src="@/assets/mockup.svg" alt="Discover photo" class="main-img"/>
        </div>
        <div class="content-info">
          <div class="title">
            <p>Download our app</p>
            <h1>Get The Groceries App Order More Easily.</h1>
          </div>
          <p class="info">
            Lorem ipsum dolor sit amet consectetur adipisicing elit. Quos, laboriosam! Suscipit commodi similique ullam minus.
          </p>
          <div class="badges">
            <img src="@/assets/google-play-badge.png" alt="App store">
            <img src="@/assets/app-store-badge.png" alt="App Store">
          </div>
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
.main{
  height: 100%;
}

.hero-content{
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding: $padding;
  
  .hero{
    margin-top: 4rem;
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
      font-size: 4.5rem;
      font-weight: bolder;
      line-height: 5.5rem;
      margin: 1rem 0;
      span{
        color: #F54748;
      }
    }

    .hero-info{
      width: 30rem;
      font-size: 1.1rem;
      line-height: 30px;
      letter-spacing: 0.5%;
      margin: 0;
      padding: 0;
    }

    .buttons{
      display: flex;
      margin: 2rem 0;

      .cta{
        height: 4.2rem;
        width: 12rem;
        border-radius: 12px;
        background: $red;
        color: #fff;
        display: flex;
        justify-content: center;
        align-items: center;
        font-weight: $medium;
        font-size: 1.25rem;
      }

      .order-process{
        display: flex;
        align-items: center;
        margin-left: 2rem ;

        .order-process-btn{
          width: 4.2rem;
          height: 4.2rem;
          border-radius: 50%;
          box-shadow: 0px 20px 49px -10px rgba(0, 0, 0, 0.08);
          display: flex;
          justify-content: center;
          align-items: center;
        }

        p{
          font-size: 20px;
          padding-left: 1rem;
        }
      }
    }

  }

  .hero-image{
    display: flex;
    justify-content: right;
    position: relative;

    :not(:first-child){
      position: absolute;
    }

    #pic-1{
      top: 20%;
      left: -5%;
    }

    #pic-2{
      top: 10%;
      right: -15%;
    }

    #abstract{
      top: 30%;
      right: -10%;
      height: 10rem;
      width: 8rem;
      transform: rotate(-8.37deg);
    }
  }
}

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

  @media (max-width: 1000px){
    padding: 1rem;
  }
}

.title{
    text-align: center;
    p, h1{
      margin: 0;
    }

    p{
      color: $red;
    }

    h1{
      width: 32rem;
      line-height: 3rem;
      display: inline-block;
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
      width: 15rem;
      height: 16rem;
    }
  }
}

.why-choose-us-container, .home-delivery-container{
  background: #fff;

  .why-choose-us-content{
    display: flex;
    align-items: center;
    gap: 10rem;
    .content-image{
      position: relative;
      .main-img{
        width: 34.5rem;
        height: 41rem;
      }

      .content-card{
        position: absolute;
        top: 16rem;
        right: -5rem;
      }
    }
    .content-info{
      .title{
        margin-bottom: 1.5rem;
        text-align: left;
        p{
          color: #03A66B;
        }
        h1{
          width: 20rem;
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
      }
    }
  }
}

.home-delivery-content{
  // display: grid;
  // grid-template-columns: 1fr 1fr;
  // align-items: center;

  display: flex;
  align-items: center;
  gap: 6rem;
  .main-img{
    width: 36rem;
    justify-content: flex-end;
  }

  .content-info{
    .title{
      text-align: left;
      h1{
        width: 30rem;
      }
      p{
        color: #F9BA45;
      }
    }

    .info{
      width: 30rem;
    }


    .explore-now-btn{
      border: 1px solid $red;
      border-radius: 8px;
      background: none;
      color: $red;
      font-size: 1rem;
      font-weight: $medium;
      width: 10rem;
      height: 3rem;
      margin-top: 1.5rem;
    }
  }
}

.sign-up-container{
  padding: 0 7rem;
  height: 47rem;
}

.sign-up-content{
  display: grid;
  grid-template-columns: 1fr 1fr;
  align-items: center;

  .content-info{
    .title{
      text-align: left;
      h1{
        width: 25rem;
      }
    }
  }

  .badges{
    display: flex;
    gap: 1rem;
  }
}

.hero-content,
.what-we-serve-content, 
.why-choose-us-content, 
.home-delivery-content{
  @media (max-width: 1024px){
    display: flex;
    flex-wrap: wrap-reverse;
    justify-content: center;
    padding: 1rem;
  }
}

.why-choose-us-content, .what-we-serve-content{
  @media (max-width: 1024px) {
    flex-wrap: wrap;
  }
}

.content-info, .hero-content{
  @media (max-width: 1024px){
    margin: 0 auto;
  }
     
}


</style>