<template>
  <div class="about">
    <div class="about-image">
      <img src="@/assets/fruits.svg" alt="fruits">
    </div>
    <div class="about-content">
      <h1 class="title">About Us</h1>
      <div class="info">
        <p>
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti. 
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
        </p>
        <h4>Mission</h4>
        <p>
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti.
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen voluptatum deleniti. 
          At vero eos et accusamus et iusto odio dignissimos ducimus blanditiis praesen.
        </p>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.about{
  display: flex;
  align-items: flex-start;
  @media only screen and (max-width: 800px){
    padding: 1rem;
    justify-content: flex-start;
    flex-direction: column-reverse;
  }
}


.about-image{

  @media only screen and (max-width: 800px){
    display: none;
  }

  img{
    height: 55vw;
  }
}


.title{
  font-size: 74px;
  color: $red;
  @media only screen and (max-width: 1200px){
    font-size: 46px;
  }

  @media only screen and (max-width: 600px){
    text-align: center;
  }
}

.info{
  width: 70%;
  line-height: 30px;

  @media only screen and (max-width: 1200px){
    width: 100%;
  }

  @media only screen and (max-width: 600px){
    text-align: center;
  }

  p{
    font-size: 18px;
  }
}

</style>
