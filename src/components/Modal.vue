<template>
    <div class="modal-container">
        <transition name="slide">
            <div class="modal">
                <img src="@/assets/ok.svg" alt="Ok svg">
                <p>Your email has been sent. We will reach out to you shortly.</p>
            </div>
        </transition>
    </div>
</template>

<style lang="scss" scoped>

.slide-leave-active,
.slide-enter-active {
  transition: 1s;
}
.slide-enter {
  transform: translate(100%, 0);
}
.slide-leave-to {
  transform: translate(-100%, 0);
}

.modal-container{
    position: absolute;
    width: 90%;
    height: 100%;
    top: 12%;
    z-index: 10;
}
.modal{
    position: fixed;
    left: 50%;
    transform: translateX(-50%);
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 0.5rem;
    width: 36%;
    margin: 0 auto;
    background: #fff;
    border-left: 4px solid #03A66B;
    box-shadow:  0px 60px 100px -10px rgba(86, 0, 0, 0.08);

    

    @media only screen and (max-width: 1100px){
        width: 50%;
    }

    @media only screen and (max-width: 600px){
        width: 90%;
    }

    img{
        width: 36px;
        height: 36px;
    }
}
</style>