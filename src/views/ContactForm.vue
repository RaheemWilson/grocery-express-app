<template>
  <div class="contact-form-container">
    <Modal v-if="show"></Modal>
    <div class="business-contact" data-aos="fade-right" data-aos-duration="800">
      <h2>Get in touch</h2>
      <p>We'd love to hear from you. Our friendly team is here to chat.</p>
      <div class="contact-details">
        <div class="detail">
          <img src="@/assets/mail_outline.svg" alt="Mail icon">
          <div>
            <p class="detail-title">Chat to us</p>
            <p class="detail-desc">Our team is here to help.</p>
            <a href="mailto:groceryexpress@gmail.com" class="detail-link">groceryexpress@gmail.com</a>
          </div>
        </div>
        <div class="detail">
          <img src="@/assets/place_black.svg" alt="Location icon">
          <div>
            <p class="detail-title">Business place</p>
            <p class="detail-desc">Come say hello at our business place.</p>
            <p class="detail-link">41 Kingston Street <br> Kingston, Jamaica</p>
          </div>
        </div>
        <div class="detail">
          <img src="@/assets/call_black.svg" alt="Phone icon">
          <div>
            <p class="detail-title">Phone</p>
            <p class="detail-desc">Monday - Saturdays from 8am to 6pm </p>
            <a href="tel:+1-876-888-8888" class="detail-link">+1 (876) 888-8888</a>
          </div>
        </div>
      </div>
    </div>
    <div class="contact-us">
      <div class="contact-us-content">
        <h2>Contact us today</h2>
        <form class="contact-form" @submit.prevent="handleSubmit">
          <div>
            <label for="name">Name</label>
            <input type="text" name="name" id="name" required>
          </div>
          <div>
            <label for="email">Email</label>
            <input type="email" name="email" id="email" required>
          </div>
          <div>
            <label for="telephone">Phone number</label>
            <input type="telephone" name="telephone" id="telephone" required>
          </div>
          <div>
            <label for="message">How can we help?</label>
            <textarea name="message" id="message" cols="30" rows="10" required></textarea>
          </div>
          <button type="submit">Send message</button>
        </form>
      </div>
    </div>
  </div>
</template>

<script>
import Modal from '@/components/Modal.vue'
export default {
  name: 'Contact Form',
  components: { Modal },
  data(){
    return {
      show: false
    }
  }, 
  methods: {
    handleSubmit(){
      this.show = true

      setTimeout(() => {
        this.show = false
      }, 4000);
    }
  }
}
</script>

<style lang="scss" scoped>

.contact-form-container{
  display: flex;
  gap: 6rem;
  padding: $padding;
  max-width: 100%;
  @media only screen and (min-width: 801px) and (max-width: 1200px){
    gap: 1rem;
    padding: 1rem;
  }

  @media only screen and (max-width: 800px){
    flex-wrap: wrap-reverse;
    justify-content: center;
    padding: 0;
  }


  .business-contact{
    background: $red;
    color: #fff;
    padding: 0 2rem;
    width: 30%;

    @media only screen and (max-width: 600px){
      width: 90%;
    }

    img{
      filter: invert(1);
      margin-top: 5px;
    }

    .contact-details{
      margin-top: 2rem;
      .detail{
        display: grid;
        grid-template-columns: 30px 2fr;
        column-gap: 1rem;
        margin-bottom: 20px;
  
        .detail-title{
          font-size: 1.1rem;
          font-weight: bold;
          margin: 0;
        }
  
        .detail-desc{
          margin: 5px 0 25px;
        }
  
        .detail-link{
          color: #fff;
          font-weight: $medium;
          font-weight: bold;
        }
      }
    }

  }
  

  .contact-us{
    display: flex;
    align-content: center;
    justify-content: center;
    padding: 4rem 5rem;
    padding-right: 0;
    max-width: 100%;
    @media only screen and (min-width: 801px) and (max-width: 1200px){
      padding: 1rem;
    }
    @media only screen and (max-width: 800px){
      padding: 0;
    }
    
    input, textarea{
      display: block;
      width: 30rem;
      padding: 0 12px 0 16px;
      margin-top: 5px;
      font-size: 16px;
      font-family: $font-family;
      border: 1px solid rgb(46, 46, 46, 0.25);
      border-radius: 8px;
      resize: none;
      color: #2e2e2e;
      @media only screen and (max-width: 600px){
        width: 80vw;
      }

    }

    input:focus, textarea:focus{
      border: 1px solid #2e2e2e;
    }

    input{
      height: 48px;
    }

    label{
      font-weight: $medium;
      font-size: 18px;
    }

    form > div{
      margin: 20px 0;
    }

    form > button{
     background: $red;
     border: none;
     border-radius: 8px;
     width: 100%;
     height: 48px;
     text-align: center;
     font-size: 16px;
     color: #fff;
     font-weight: bold;
    }
  }

  
}

</style>