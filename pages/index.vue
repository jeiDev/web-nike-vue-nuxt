<template>
    <div class="container">
      <section class="first">
          <div class="background">
              <div class="box-image">
                <img src="~/assets/images/blackground-one.jpg" alt="blackground-one">
                <div class="gradient"></div>
              </div>
              <div class="medio-div"></div>
          </div>
          <div class="box-"></div>
      </section>
    </div>
</template>

<script>

export default {
  components: {

  }
}
</script>

<style scoped>
  .container{
    width: 100vw;
  }

  .container>.first{
    width: 100%;
    height: 100vh;
    overflow: hidden;
    box-sizing: border-box;
    position: relative;
  }

  .container>.first>.background{
    position: absolute;
    width: 100%;
    height: 100%;
    left: 0;
    top: 0;
  }

  .container>.first>.background>div{
    height: 100%;
  }

  .container>.first>.background>.box-image{
    width: 100%;
  }

  .container>.first>.background>.box-image>img{
    position: absolute;
    width: 100%;
    height: 100%;
    object-fit: fill;
    bottom: 0;
  }

  .container>.first>.background>.box-image>.gradient{
    position: relative;
    left: 0;
    top: 0;
    width: 100%;
    height: 100%;
    background-color: rgba(0,0,0,.2);
  }

  .container>.first>.background>.medio-div{
    position: absolute;
    left: 50%;
    top: 0;
    height: 100%;
    width: 0%;
    background-color: #df1934;
    animation: .5s widthDivMedio forwards;
  }

  @keyframes widthDivMedio {
    from {
      left: 50%;
      width: 0%;
    }
    to {
      left: 0%;
      width: 50%;
    }
  }
</style>
