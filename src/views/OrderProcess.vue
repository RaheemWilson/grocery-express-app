<template>
    <div class="order-process">
        <iframe  src="https://www.youtube.com/embed/PImGM4_o61o" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
    </div>
</template>

<style lang="scss" scoped>
.order-process{
    display: flex;
    align-items: center;
    justify-content: center;
    padding: 2rem 0;
    iframe{
        width: 60vw;
        height: 40vw;
        @media only screen and (max-width: 600px){
            width: 80vw;
            height: 40vw;
        }

    }
    // width="560" height="315"
}
</style>

