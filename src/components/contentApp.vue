<template>

  <div class="container">
    <div class="box">
        <div class="line">
            <div class="circle__top"></div>
            <div class="obj"></div>
            <div class="circle__bottom"></div>
        </div>
        
        <p class="subtitle">Точка назначения:</p>
        <!-- <h1 class="title">марс</h1> -->

        <!-- <div class="section"> -->
            <!-- <video autoplay loop muted>
                <source src="./video/marss.mp4" type="video/mp4">
            </video> -->
            <h2 class="mars">МАРС</h2>
            
        <!-- </div> -->


    </div>
  </div>
    


</template>
<style lang="scss">
.box{
    position:absolute;
    display: flex;
    flex-direction: column;
    align-items: flex-start;
}
.line{
    position: relative;
    left: -20px;
    top: 120px;
    
}
.circle__top{
    position: absolute;
width: 12px;
height: 12px;
left: 5px;
top: -10px;
border-radius: 50%;
background: #D9D9D9;
}
.circle__bottom{
    position: absolute;
width: 12px;
height: 12px;
left: 5px;
top: 580px;
border-radius: 50%;
// background: #D9D9D9;
animation-name: circle__bottom;
animation-delay:1.7s;
animation-duration: 1.1s;
animation-fill-mode: forwards;
}
@keyframes circle__bottom{

    0%{
        color: transparent;
    }
    80%{
        color: red;

    }
    100%{
        background: #D9D9D9;
    }
}

.obj{
    width: 2px;
    height: 2px;
    background: #D9D9D9;
    position: absolute;
    top: -10px;
    left:10px;
    animation-name: move;
    animation-duration: 2s;
    animation-fill-mode: forwards;
}
@keyframes move{

    from{
        height: 30px;
        border-radius: 0%;
    }
    to{
        height: 597px;
    }
}



.subtitle{
    margin-top: 130px;
    margin-left: 40px;
    font-size: 36px;
    font-weight: 500;
    color: transparent;
    font-family: 'Montserrat';
    animation-name: subtitle;
    animation-duration: 3s;
    animation-fill-mode: forwards;
    font-family: 'Montserrat';
    font-style: normal;
    font-weight: 500;
}
@keyframes subtitle{

    from{
        color: transparent;
    }

    to{
        color: red;
    }
}

.mars{
    font-weight: 900;
    color: transparent;
    font-size: 400px;
    /* margin: 0; */
    margin-top: -90px;
    margin-left: 30px;
    letter-spacing: -10px;
    opacity: 60%;
    animation-name: mars;
    animation-duration: 3s;
    animation-fill-mode: forwards;
    animation-delay:1.7s;
    
}
@keyframes mars{

    from{
        
    }

    to{
        color: rgb(223, 200, 126);
    }
}

</style>