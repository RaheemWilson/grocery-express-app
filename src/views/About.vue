<template>
  <div class="about">
    <div>
      <img src="@/assets/fruits.svg" alt="fruits">
    </div>
    <div class="info">
      <h1>About Us</h1>
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
</template>

<style lang="scss" scoped>
.about{
  display: flex;
  gap: 8rem;
  padding-right: 7rem;
  
  img{
    height: 50rem;
  }

  .info{
    text-align: center;
    h1{
      color: $red;
      font-size: 4.5rem;
    }

    p{
      width: 45rem;
      line-height: 2rem;
    }

    h4{
      margin-top: 5rem;
    }
  }
}
</style>
