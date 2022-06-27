<template>
  <section>
        <subNavbar></subNavbar>
    </section>
        <div class="container-fluid main-background"></div>
            <section class="container-fluid container main-products">
              <div class="main">
                  <div class="container-md products">
                      <div class="row">
                          <div class="col main-logo-title mb-3 ">
                              <h1 class="mt-5 text-center fs-1 fw-bolder">關於</h1>
                          </div>
                      </div>
                      <div class="row p-5">
                        <p><b>＃什麼是 Minecraft?</b><br>
                            Minecraft 是由瑞典遊戲設計師，Markus Persson 單獨開發的沙盒遊戲。
                            其後他於 2009年成立瑞典公司 Mojang 繼續開發並發行。在 2014年9月，
                            他把 Minecraft 以25億美元賣給微軟。至2020年統計，Minecraft統計全球
                            使用者已經到達1.31億人，在台灣學生幾乎都知道或己經玩過，甚至於學校
                            等教育單位都以「玩麥塊學程式，的主题，引導小朋友程式邏輯學習。</p>
                        <p><b>＃為何要舉辦麥塊建築大賽？</b><br>
                            當身為家長的我們，看到從2020年起許多大學、高中、國中開始有不同麥塊
                            愛好者，因疫情設計虛擬校園及虛擬畢業典禮，我們認為可以引導小朋友在
                            創造及程式學習上使用Minecraft，並因應108新課綱高中以下可能需要學習歷
                            程(研習/獎勵/證書)在未來升學使用，故與國立臺北護理健康大學合作並邀請
                            全台大專院校共襄盛舉，讓小朋友在開心的創作中參與競賽，獲得學習歷程證
                            明也充足自己團隊協做的信心，因此舉辦麥塊建築大賽。</p>
                        <p><b>Minecraft 是一個這樣的遊戲：</b><br>
                        「 Minecraft 」（我的世界）是一款風靡全世界的沙盒遊戲，
                          玩家在遊戲裡可以跟整個世界進行各種互動，從挖礦、生存到建築，創造出屬於
                          自己獨一無二的世界。(摘自: 電腦玩物, Minecraft 中文教育版推出！免費下
                          載教學與特色介紹)<br>
                            「讓人們可以建造屬於自己的 Minecraft，這很重要」，Majong 研究中心主
                            管賽克斯·佩爾森（Saxs Persson）表示，「這款遊戲最強調的就是個人體驗」。<br>
                            「這樣能鼓勵更多的人們去建造自己想要建造的東西」，佩爾森說道。<br>
                            (摘自: 科技報橘, 《Minecraft》: 為什麼一款沒有目標、點陣風格的遊戲可
                            以風靡全世界？)<br>
                            你可能還在問: "為什麼 Minecraft 這樣受小朋友歡迎呢?" 或許，當您看到
                            小朋友的建築作品時，可以得到你想要的答案。</p><br>
                        <p><b>#一個極具潛質的教育工具，也是個遊戲!</b><br>
                            以上內容部分節錄於第一屆「賽馬會教師創新力量計劃」參與老師 Jack Seto Wah Sang 於 medium 中所發表的文章</p>
                      </div>
                  </div>
              </div>
              <img class="alex" src="../assets/Alex.png" alt="">
          </section>
    <my-footer></my-footer>
</template>

<script>
import SubNavbar from '../components/SubNavbar.vue';
import MyFooter from '../components/MyFooter.vue';

export default {
  name: 'AboutView',
  components: {
    SubNavbar,
    MyFooter,
  },
  data() {
    return {
      background: require('../assets/bg/2022-04-22_02.33.39.png'),
    };
  },
};
</script>

<style scoped>
.alex{
    float: right;
    position: relative;
}
.about{
  z-index: -1;
    background-image: url('../assets/bg/2022-04-22_02.33.39.png');
    background-repeat: no-repeat;
    background-size: 100%;
}
.main-background{
    height: 100vh;
    background: no-repeat center url('../assets/bg/2022-04-22_02.33.39.png');
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}
.main{
    position: relative;
    box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    background-color: #fff;
    top: -70vh;
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
      .alex{
          display: none;
      }
    }

    @media screen and (max-width: 786px){
        /* .main-background{
            height: 50vh;
            background-size: cover;
        } */
        .main{
            box-shadow: none ;
            border-radius: 0;
        }
    }
    /* .container{
    border-radius: 5px;
    background-color: rgba(252, 246, 246, 0.912);
    box-shadow: 0px 0px 100px 10PX rgba(105, 103, 103, 0.556);
    border: 1px solid rgba(174, 171, 171, 0.642);
    margin-top: 370px;
    margin-bottom: 100px;
}
@media screen and (max-width: 786px){
  .container{
    margin-top: 230px;
    margin-bottom: 15px;
  }
  .alex{
            width: 90px;
        }
} */
</style>
