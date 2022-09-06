<template>
    <header>
                
                    <div class="header-top">
                        <nav class="menu">
                            <div class="menu__logo">
                                <a class="menu__link" href="#"></a>
                            </div>
                             <nav class="menu__nav">
                                <ul class="menu__list">
                                    <li class="menu__item">
                                        <a href="#" class="menu__link">о марсе</a>
                                    </li>
                                    <li class="menu__item">
                                        <a href="#" class="menu__link">процесс</a>
                                    </li>
                                    <li class="menu__item">
                                        <a href="#" class="menu__link">билеты</a>
                                    </li>
                                    <li class="menu__item">
                                        <a href="#" class="menu__link">новости</a>
                                    </li>
                                    <li class="menu__item">
                                        <a href="#" class="menu__link">контакты</a>
                                    </li>
                                    <div>
                                        <button class="menu__button ">
                                            <a class="menu__link--btn" href="#" >Купить билеты</a>
                                        </button>
                                        <button class="menu__btn">
                                            <span class="row"></span> 
                                        </button>
                                    </div>
                                </ul>
                            </nav>
                        </nav>
                    </div>
                
                
            </header>
</template>

<style lang="scss">

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu{
    position: relative;
    display: flex;
    justify-content: space-between;
    color: wheat;
    align-items: center;
    margin-top: 60px;

    &__logo{
        background-image: url(../img/Mars.svg);
        width: 82px;
        height: 36px;
        
        @media (max-width: 400px){
            font-size: 25px;
        }
    }

    &__btn{
        display: none;
        height: 25px;
        width: 30px;
        border: none;
        padding: 0;
        background-color:transparent;
        position: absolute;
        right: 30px;
        top: 40px;
        
        span{
            display: block;
            background-color: rgb(238, 236, 236);
            height: 5px;
            width: 100%;
        }

        @media (max-width: 1000px){
            display: inline-block;
        }
    }

    &__nav{
        display: flex;
    }
    
    &__list{
        display: flex;
        align-items: center;
        :not(:last-child){
            margin-right:30px;
          }
        @media (max-width: 1000px){
            display: none;
        }
    }
    


    &__item{
        font-weight: 500;
        font-size: 16px;
        line-height: 20px;

        &--logo{
            font-size: 36px;
            font-weight: 600;
        }
    }

    &__button{
        color: black;
        padding: 10px 10px;
        background-color: #F2E1C2;
        margin: 0;
        border-radius: 5px;
        border: none;
        @media (max-width: 1000px){
            margin-right: 70px;
        }
        
    }

    &__link{
        color: #F2E1C2;
        font-weight: 500;
        font-size: 16px;
        text-transform: uppercase;
        &--btn{
            color: black;
            font-weight: 500;
            font-size: 16px;
            text-transform: uppercase;
            border: none;
        }
        
    }
    &__link:hover{
        color: red;
        
    }

}

</style>