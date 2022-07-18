<template>
    <section>
        <subNavbar></subNavbar>
    </section>
    <section class="container-fluid main-background"></section>
    <section class="container-fluid container main-products">
        <div class="main">
            <div class="container-md products">
                <div class="row">
                    <div class="col main-logo-title mb-3 ">
                        <h1 class="mt-5 text-center fs-1 fw-bolder">元宇宙商圈</h1>
                    </div>
                </div>
                <div class="row card-items g-5 p-3 mb-3 justify-content-center text-center">
                    <div class="text">
                        coming soon...
                    </div>
                    <!-- <img class="text" src="https://fakeimg.pl/200x100/?retina=1&text=coming soon...&font=noto"> -->
                    <img class="alex" src="../assets/Alex.png" alt="">
                    <img class="creeper" src="../assets/Creeper.png" alt="../assets/Creeper.png">
                </div>
            </div>
        </div>
        <img class="herobrine" src="../assets/Donkey.png" alt="">
    </section>

  <MyFooter></MyFooter>
</template>

<script>
import SubNavbar from '../components/SubNavbar.vue';
import MyFooter from '../components/MyFooter.vue';
import ProductItem from '../components/ProductItem.vue';

export default {
  name: 'MineverseView',
  components: {
    SubNavbar,
    MyFooter,
    ProductItem,
  },
  data() {
    return {
    };
  },
};
</script>

<style scoped>
.text{
    color:#fff;
    text-shadow: 0 0 5px #999;
    font-size: 3rem;
    padding: 0;
}
.alex{
    width: 200px;
    height: auto;
}
.herobrine{
    width: 200px;
    float: right;
    position: relative;
    bottom: 100px;
    right: 30px;
}
.creeper{
    display: none;
}
/* main */
.main-background{
    height: 100vh;
    background: no-repeat center url('../assets/bg/2022-04-22_02.49.37.png');
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}

.main{
    /* position: relative; */
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    background-color: #fff;
    margin-top: -70vh;
    margin-bottom: 20vh;
    border-radius: 10px;
}
    .main-products{
        padding: 0;
    }
    /* @media screen and (max-width: 1400px){
        .main{
            box-shadow:0 0px rgba(0,0,0,0);
        }
    } */

    @media screen and (max-width: 992px){
        
    .text{
        color:#fff;
        text-shadow: 0 0 5px #999;
        font-size: 2rem;
    }
    /* .text{
        display: none;
    } */
    
    .herobrine{
        display: none;
    }
    .alex{
        display: none;
    }
    .creeper{
        display: block;
        width: 200px;
    }

}

    @media screen and (max-width: 576px){
        
        /* .main-background{
            height: 50vh;
            background-size: cover;
        } */
        .main{
            box-shadow: none ;
            border-radius: 0;
        }
        
    }
    
    /* 卡片內容 */
    /* .card {
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
    .card:hover {
        cursor: pointer;
        transform: scale(1.1);
        transition: transform 0.5s ease;
    } */
    /* .item-img{
        width: 100%;
    } */
    /* .card-img-top{
        width: 100%;
        height: 20rem;
        object-fit:  scale-down;
    } */

    .bi-star-fill {
    color: rgb(255, 208, 0);
    }
    
    
</style>