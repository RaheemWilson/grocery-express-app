<template>
  <div class="about">
    <h1>This is a service page</h1>
  </div>
</template>

<style scoped>
/* .main{
  height: 100%;
}

.hero-container{
  display: grid;
  grid-template-columns: 1fr 1fr;
  padding: $padding;
  
  .hero-content{
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

    img{
      width: 40rem;
      height: 34rem;
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
  /* first breakpoint*/
  

  /* display: grid;
  grid-template-columns:
    repeat(auto-fill,
      minmax(clamp(clamp(clamp(  
            100%/(var(--n) + 1) + 0.1%,
              (var(--w1) - 100%)*1000,
            100%/(var(--m) + 1) + 0.1%), 
              (var(--w2) - 100%)*1000,
            100%/(var(--p) + 1) + 0.1%), 
              (var(--w3) - 100%)*1000,
            100%), 1fr));
  align-items: center;

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
  } */
     
/* } */

</style>