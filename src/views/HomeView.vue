/* eslint-disable */
<template>
  <MainNavbar></MainNavbar>
  <latest-news></latest-news>
  <!-- introduction -->
  <div class="intro">
    <div class="container p-5 introduction">
      <div class="row d-flex justify-content-evenly text-center fs-1">
        <div class="col col-md-5 col-lg-4 mb-5">
          <div class="mb-5"><img src="@/assets/homepage/zombie.png" alt="create-picture"></div>
          <div class="fs-4">有時生存有時創造</div>
        </div>
        <div class="col col-md-5 col-lg-4 mb-5">
          <div class="mb-5"><img src="@/assets/homepage/group.png" alt="group-picture"></div>
          <div class="fs-4">耐人尋味的關卡</div>
        </div>
        <div class="col col-md-5 col-lg-4 mb-5">
          <div class="mb-5"><img src="@/assets/homepage/castle.png" alt="build-picture"></div>
          <div class="fs-4">想蓋自己的小天地？那就蓋吧！</div>
        </div>
      </div>
    </div>
  </div>
  <!-- icons -->
  <div id="info" class="container p-5">
    <div class="row fw-bold">
      <div class="col-md-6 col-sm-12 row text-center mb-5">
        <div class="title mb-5 text-center fs-1 fw-bold">社群平台</div>
        <a class="col-6" href="https://www.facebook.com/codedriven/" target="_blank"><img src="@/assets/homepage/fbicon.png" alt="粉專"></a>
        <a class="col-6" href="" target="_blank">
          <img src="@/assets/homepage/discord.png" alt="discord">
        </a>
      </div>
      <div class="col-md-6 col-sm-12 row text-center mb-5">
        <div class="title mb-5 text-center fs-1 fw-bold">合作夥伴</div>
        <a class="col-6" href="https://www.sce.pccu.edu.tw/" target="_blank"><img src="@/assets/homepage/ntcicon.png" alt="文大"></a>
        <a class="col-6" href="https://www.codedriven.org/" target="_blank"><img src="@/assets/homepage/codedrivenicon.png" alt="程式驅動"></a>
      </div>
    </div>
  </div>
  <!-- <div id="server">
    <div class="container p-5 pt-0">
      <div class="d-flex flex-column justify-content-center">
        <div class="text-center mb-5 fs-1 fw-bold">伺服器狀態</div>
        <a href="https://minecraft-mp.com/server-s303741"
        target="_blank"><img :src="leaderboard" class="w-100" alt="leaderboard"></a>
      </div>
    </div>
  </div> -->

  <my-footer></my-footer>
</template>

<script>
import MainNavbar from '@/components/Home/MainNavbar.vue';
import LatestNews from '@/components/Home/LatestNews.vue';
import MyFooter from '../components/MyFooter.vue';

export default {
  name: 'HomeView',
  data() {
    return {
      image: require('../assets/minecraftserver.png'),
      leaderboard: 'https://minecraft-mp.com/leaderboard-303741-6.png',
    };
  },
  components: {
    MyFooter,
    MainNavbar,
    LatestNews,
  },
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');

nav ul {
display: flex;
justify-content: center;
overflow: hidden;
}

nav a{
display: inline-block;
width: 200px;
height: 70px;
padding: 15px 0 15px 0;
color: rgb(255, 255, 255);
}

nav a:hover{
color: rgb(255, 255, 255);
border-bottom: 3px solid yellow;
}

.burgar{
color: var(--white);
font-size: 1.5rem;
display:none;
}

.sticky{
position: fixed;
top:0;
background:rgba(0, 0, 0,0.7);
transition:0.5s;
z-index: 1;
}

.sticky a{
color:var(--white);
}

.sticky a:hover{
  color:var(--white);
}

.navposition {
  position: relative;
  top: 370px;
}
</style>
