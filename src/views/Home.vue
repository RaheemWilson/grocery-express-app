<template>
  <div class="main">
    <Header></Header>
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
        <img src="@/assets/pic-1.svg" alt="card" id="pic-1">
        <img src="@/assets/pic-2.svg" alt="card" id="pic-2">
        <img src="@/assets/abstract.svg" alt="abstract" id="abstract">
      </div>
    </div>
    <div class="what-we-serve-content">
      <div class="title">
        <p>What we serve</p>
        <h1>Fruit And Vegetable Delivered To Your Home</h1>
      </div>
      <div class="cards">
        <div class="card">
          <img class="card-icon" src="@/assets/delivery-icon.svg" alt="icon">
          <p class="card-title">Free shipping</p>
          <p class="card-desc">Enjoy order in a hand using the freshness of groceries</p>
        </div>
        <div class="card">
          <img class="card-icon" src="@/assets/returns-icon.svg" alt="icon">
          <p class="card-title">5 days return</p>
          <p class="card-desc">If you get rotten items - return immediately to us.</p>
        </div>
        <div class="card">
          <img class="card-icon" src="@/assets/secure-icon.svg" alt="icon">
          <p class="card-title">Secure checkout</p>
          <p class="card-desc">Pay for your fruits and vegetables without a hassle.</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Header from '@/components/Header.vue'

export default {
  name: 'Home',
  components: {
    Header
  }
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

.what-we-serve-content{
  margin-top: 7rem;
  padding: 2rem;
  background: $light-red;

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
}


</style>