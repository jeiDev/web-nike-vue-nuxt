<template>
   <header>
       <div class="column left">
           <div class="box-logo">
               <Logo />
            </div>
           <div class="box-menu">
               <nav>
                   <ul id="menuHeader">
                        <li v-for="(item, index) in menu" :key="index" @mouseover="mouseEnterMenu(index)" @mouseout="mouseOutMenu(index)" class="item">
                           {{item.title}}
                           <div v-if="item.active" class="line active"></div>
                           <div v-if="!item.active" class="line"></div>
                        </li>
                   </ul>
               </nav>
           </div>
       </div>
       <div class="column right">
           <div class="box-icon">
               <ShoppingIcon />
               <SearchIcon />
           </div>
           <div class="box-text">
               <ul>
                   <li>LOGIN</li>
                   <li>EN</li>
               </ul>
           </div>
           <div class="box-open-menu">
               <div class="line one"></div>
               <div class="line two"></div>
           </div>
       </div>
   </header>
</template>

<script>
import Logo from '../Logo'
import ShoppingIcon from '../svg/shoppingCart'
import SearchIcon from '../svg/search'


export default {
    data() {
        return {
            menu: [{title: "NIKE", active: true}, {title: "NIKE+", active: false}, {title: "VANS", active: false}, {title: "CONVERSE", active: false}]
        }
    },
    components: {
        Logo,
        ShoppingIcon,
        SearchIcon
    },
    methods: {
        mouseEnterMenu(i){
            let items = document.getElementById("menuHeader").querySelectorAll(".item");

            if(items[i]) items[i].querySelector(".line").style.width = "100%";
        },
        mouseOutMenu(i){
            let items = document.getElementById("menuHeader").querySelectorAll(".item");

            if(items[i]) items[i].querySelector(".line").style.width = "0%";
        }
    }
}
</script>

<style>
    header{
        width: 100vw;
        height: 90px;
        min-height: 90px;
        position: fixed;
        overflow: hidden;
        padding: 20px;
        display: flex;
        align-items: center;
        box-sizing: border-box;
    }

    header>.column{
        min-width: 50%;
        max-width: 50%;
        flex: 1 1 auto;
        display: flex;
        align-items: center;
    }

    header>.left>.box-menu ul{
        display: flex;
    }

    header>.left>.box-menu ul>li{
        margin-left: 70px;
        cursor: pointer;
        font-weight: 500;
    }

    header>.left>.box-menu ul>li>.line{
        width: 0;
        height: 2px;
        background-color:white;
        transition: all ease .3s;
    }

    header>.left>.box-menu ul>li>.line.active{
         width: 100%;
    }


    header>.left>.box-menu ul>li:first-child{
        margin-left: 0;
    }

    header>.left>.box-logo{
        margin-right: 45px;
    }

    header>.left>.box-logo .logo-nike{
        height: 40px;
        width: 60px;
        object-fit: contain;
    }

    header>.right{
        justify-content: flex-end;
    }

    header>.right>.box-icon{
        display: flex;
        align-items: center;
    }

    header>.right>.box-icon svg{
        height: 19px;
        width: 19px;
        margin-right: 30px;
        cursor: pointer;
        position: relative;
        top: 2.5px;
    }

    header>.right .box-text>ul{
        display: flex;
        align-items: center;
        padding-left: 0;
    }

    header>.right .box-text>ul>li{
        margin-right: 30px;
        cursor: pointer;
    }

    header>.right .box-open-menu{
        padding-top: 5px;
        display: flex;
        flex-direction: column;
        align-items: flex-end;
        cursor: pointer;
    }

    header>.right .box-open-menu>.line{
        height: 1.6px;
        background-color: white;
        margin-bottom: 4px;
    }

    header>.right .box-open-menu>.line.one{
        width: 28px;
    }

    header>.right .box-open-menu>.line.two{
        width: 20px;
    }
</style>