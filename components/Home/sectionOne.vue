<template >
    <section class="first">
          <div class="background">
              <div class="box-image">
                <img src="~/assets/images/blackground-one.jpg" alt="blackground-one">
                <div class="gradient"></div>
              </div>
              <div class="medio-div"></div>
          </div>
          <div class="box-info margin-box content-first">
            <div class="left max-width">
                <div class="box-price">
                  <span class="symbol">$</span>
                  <span>210</span>
                </div>
                <div class="box-color">
                  <div class="white"></div>
                  <div class="black"></div>
                </div>
                <div class="box-info min-font-size">
                  <p>COMET PED/BLACK<br />WHITE/RELENTLESS</p>
                </div>

                <div class="box-info">
                  <h3>EXPLORE</h3>
                </div>

                <div class="box-info">
                  <div class="btn-reviews">
                    <span class="btn-review">REVIEWS</span>
                  </div>
                </div>
            </div>
            <div class="center">
              <div class="box-text">
                <h2>AIR</h2>
                <h2>MAX</h2>
              </div>
              <div class="box-img">
                <img src="~/assets/images/shoe-nike-air-max.png" alt="shoe-nike-air-max" id="shoeNikeAirMaxFirst">
                <div class="shadow" id="shoeNikeAirMaxFirstShadow"></div>
              </div>
            </div>
            <div class="right max-width">
              <span>NIKE</span>
              <h3>AIR MAX<br />90 ULTRA</h3>
              <span>MEN'S SHOE</span>
              <div class="box-size">
                <div class="active">SIZE</div>
                <div class="dropdown">
                  <ul>
                    <li>5</li>
                    <li>6</li>
                    <li>7</li>
                    <li>8</li>
                    <li>9</li>
                  </ul>
                </div>
              </div>
              <div class="btn-add-cart">ADD TO CART</div>
            </div>
          </div>
      </section>
</template>

<script>
export default {
    methods: {
        initAnimatioShoeAirMax(){
            let init = false;
            let img = document.getElementById("shoeNikeAirMaxFirst")
            let shadow = document.getElementById("shoeNikeAirMaxFirstShadow")
            img.style.display = "block"

            img.addEventListener("animationend", (e) => {
                if(init) return;
                shadow.classList.add("animation")
                img.classList.add("animation")
            })
        }
    },
    mounted(){
        this.initAnimatioShoeAirMax();
    }
}
</script>

<style scoped>
    .btn-review{
        cursor: pointer;
        font-weight: 600;
    }

    .min-font-size{
        font-size: .9em;
    }

    .btn-review:hover{
        text-decoration: underline;
    }

    .first{
        width: 100%;
        height: 100vh;
        overflow: hidden;
        box-sizing: border-box;
        position: relative;
    }

    .first>.background{
        position: absolute;
        width: 100%;
        height: 100%;
        left: 0;
        top: 0;
    }

    .first>.background>div{
        height: 100%;
    }

    .first>.background>.box-image{
        width: 100%;
    }

    .first>.background>.box-image>img{
        position: absolute;
        width: 100%;
        height: 100%;
        object-fit: fill;
        bottom: 0;
    }

    .first>.background>.box-image>.gradient{
        position: relative;
        left: 0;
        top: 0;
        width: 100%;
        height: 100%;
        background-color: rgba(0,0,0,.2);
    }

    .first>.background>.medio-div{
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

    .first>.content-first{
        width: 100%;
        height: 100vh;
        overflow: hidden;
        display: flex;
    }

    .first>.content-first>.max-width{
        max-width: 180px;
        min-width: 180px;
        display: flex;
        flex-direction: column;
        justify-content: center;
    }

    .first>.content-first>.left{
        align-items: flex-end;
        text-align: right;
    }

    .first>.content-first>.left>.box-price{
        font-size: 2.5em;
        font-weight: bold;
    }

    .first>.content-first>.left>.box-price>.symbol{
        position: relative;
        font-size: .5em;
        font-weight: 100;
        left: 7px;
    }

    .first>.content-first>.left>div{
        margin-bottom: 15px;
    }

    .first>.content-first>.left>.box-color{
        display: flex;
    }

    .first>.content-first>.left>.box-color>div{
        width: 20px;
        height: 20px;
        border-radius: 50%;
        margin-right: 15px;
        cursor: pointer;
    }

    .first>.content-first>.left>.box-color>div:last-child{
        margin-right: 0;
    }

    .first>.content-first>.left>.box-color>.white{
        background-color: white;
    }

    .first>.content-first>.left>.box-color>.black{
        background-color: black;
    }

    .first>.content-first>.right{
        align-items: flex-start;
        text-align: left;
    }

    .first>.content-first>.center{
        position: relative;
        flex: 1 1 auto;
        display: flex;
        justify-content: center;
        padding-top: 15px;
    }

    .first>.content-first>.center>div{
        position: absolute;
    }

    .first>.content-first>.center>.box-text{
        display: flex;
        flex-direction: column;
    }

    .first>.content-first>.center>.box-text>h2{
        font-size: calc(100vw / 4.3);;
        text-align: center;
        margin: 0;
        line-height: 18.8vw;
    }

    .first>.content-first>.center>.box-text>h2:first-child{
        font-size:calc(100vw / 3.5);
    }

    .first>.content-first>.center>.box-img{
        position: relative;
        width: 100%;
        padding: 0 10%;
    }

    .first>.content-first>.center>.box-img>img{
        position: relative;
        width: 100%;
        object-fit: contain;
        margin-top: 10px;
        transform: rotateY(180deg);
        display: none;
        top: -100px;
        animation: 1s downShoeNike forwards;
    }

    .first>.content-first>.center>.box-img>img.animation{
        animation: 2s animateShoeNike infinite;
        top: -20px;
    }

    .first>.content-first>.center>.box-img>.shadow{
        position: relative;
        top: 5px;
        height: 20px;
        width: 90%;
        left: 7%;
        background-color: rgba(0,0,0,.5);
        border-radius: 40%;
        margin-top: 8px;
        filter: blur(5px);
    }

    .first>.content-first>.center>.box-img>.shadow.animation{
        animation: 2s animateShadowShoeNike infinite;
    }

    @keyframes downShoeNike{
        from{
            display: none;
            top: -100px;
        }

        to{
            display: block;
            top: 0px;
        }
    }

    @keyframes animateShadowShoeNike{
        0%{
            background-color: rgba(0,0,0,1);
            top: 0px;
        }

        50%{
            background-color: rgba(0,0,0,.5);
            top: 5px;
        }

        100%{
            background-color: rgba(0,0,0,1);
            top: 0px;
        }
    }

    @keyframes animateShoeNike{
        0%{
            top: 0px;
        }

        50%{
            top: -10px;
        }

        100%{
            top: 0px;
        }
    }

</style>