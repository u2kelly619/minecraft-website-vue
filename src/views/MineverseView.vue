<template>
  <div class="metaverse">
    <subNavbar></subNavbar>
    <div class="container-fluid main-background"></div>

    <div class="container-fluid background"></div>
    <div class="container-fluid">
      <div class="row justify-content-center">
        <div class="col-12 col-xxl-10 main">
          <!-- banner -->
          <div class="banner banner-pic"></div>
          <!-- logo and title -->
          <div class="text-center main-logo-title mb-3">
            <div class="logo">
              <img src="../assets/Rabbit.png" alt="" class="logo-pic" />
            </div>
            <div>
              <p class="title fs-1 fw-bold">元宇宙商圈</p>
            </div>
          </div>
          <!-- products -->
          <div class="row g-5 p-5 m-0">
            <div class="col-12 col-md-4">
              <div class="card">
                <img src="https://i.imgur.com/h7bmjlk.png" class="card-img-top" alt="..." />
                <div class="card-body">
                  <p class="card-text fs-5">Item Name</p>
                  <p class="card-text">
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                    <i class="bi bi-star-fill"></i>
                  </p>
                  <p class="card-text fs-5">$999</p>
                  <!-- <a href="#" class="stretched-link"></a> -->
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
    <my-footer></my-footer>
  </div>
</template>

<script>
import SubNavbar from '../components/SubNavbar.vue';
import MyFooter from '../components/MyFooter.vue';

export default {
  name: 'MineverseView',
  components: {
    SubNavbar,
    MyFooter,
  },
  data() {
    return {
    };
  },
};
</script>

<style scoped>
.burgar{
color: white;
font-size: 1.5rem;
display:none;
}

.sticky{
position: fixed;
top:0;
background:rgba(0, 0, 0,0.7);
transition:1s;
z-index: 1;
}

.sticky a{
color:white;
}

.sticky a:hover{
    color:white;
}

@media screen and (max-width: 786px){

.burgar{
    display: block;
    float: right;
}

.showing{
    max-height:15em;
    margin-top: 50px;
}

#navbar{
    background: rgba(0, 0, 0,0.7);
    position: fixed;
}

nav a{
    color: white;
}

nav a:hover{
    color: white;
    border-bottom: 3px solid yellow;
    }

nav ul{
    color:white;
    flex-direction: column;
    align-self:flex-end;
    max-height: 0px;
    transition: 1s;
    padding-left: 50px;
    }

nav ul li {
    box-sizing: border-box;
    width:100%;
    text-align: center;
}

}

/* main */
.main-background{
    height: 100vh;
    background: no-repeat center url('../assets/bg/2022-04-22_02.33.39.png');
    background-size: cover;
}

.main{
    background-color: #fff;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    position: relative;
    top: -70vh;
    padding: 0 !important;
    border-radius: 10px;

}

@media screen and (max-width: 1400px){
    .main{
        box-shadow:0 0px rgba(0,0,0,0);
    }
}

.banner{
    height: 200px;
    overflow: hidden;
}
.banner-pic{
    background: url('../assets/black.png');
    background-size: cover;
    background-size: 70%;
    background-repeat: no-repeat;
    background-position: center;
}

@media screen and (max-width: 786px){
    .banner{
        display: none;
    }
    .banner-pic{
        display: none;
    }
}

.main-logo-title{
    position: relative;
    top:-50px;
}

.logo-pic{
    width: 100px;
}

.card{
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
}
.card:hover{
    transform: scale(1.1);
    transition: transform 0.2s ease;
}

.bi-star-fill{
    color: rgb(255, 208, 0);
}

</style>
