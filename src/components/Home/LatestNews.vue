<template>
<div class="container-fluid main-background"></div>

<div class="container-fluid news p-5">
    <div class="row justify-content-center text-center">
      <div class="col col-md-8">
        <img src="@/assets/2022.png" class='minecraft-banner mt-5 img-fluid' alt="">
        <img src="@/assets/明道場.png" class='minecraft-banner img-fluid' alt="">
      </div>
    </div>
    <div class="row d-flex justify-content-center text-center fs-3 mt-5">
      <div class="col col-md-4">
        <div class="d-flex justify-content-center">
          <div class="border px-5 link-box">
            <span class="pixel" id="server">mbcmdu.ntc.im</span>
          </div>
          <div class="tooltip__layout" @click="flagClick">
            <span class="ms-2"><i class="bi bi-files copy"></i></span>
            <span class="tooltip__content" :class="{'show': flag}">Copied!</span>
          </div>
        </div>
      </div>
    </div>
  </div>
    <!-- expanding cards -->
  <div class="container-fluid expanding-cards">
    <div class="row justify-content-center">
      <div class="col col-md-9 d-flex">
        <div class="panel active">
            <h3>探索屬於自己的獨特世界</h3>
        </div>
        <div class="panel">
            <h3>在荒野中，踏上冒險旅途</h3>
        </div>
        <div class="panel">
            <h3>漫無目的地遊蕩，或是探尋新鮮事物</h3>
        </div>
        <div class="panel">
            <h3>整個世界任您挖掘</h3>
        </div>
        <div class="panel">
            <h3>盡情發揮想像力進行建造</h3>
        </div>
      </div>
    </div>
  </div>

  <div class="container-fluid mb-5">
    <div class="row justify-content-center">
      <h2 class="fs-1 fw-bolder my-5 text-center">最新消息</h2>
      <div class="col col-md-10 col-lg-10 accordion" id="accordionExample">
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingOne">
              <button class="accordion-button collapsed"
              type="button" data-bs-toggle="collapse"
                data-bs-target="#collapseOne"
                aria-expanded="false"
                aria-controls="collapseOne">
                [開箱]Google Home 智慧喇叭音質更好，可控制更多智能設備，讓居家變得更智慧
              </button>
            </h2>
            <div id="collapseOne"
            class="accordion-collapse collapse"
            aria-labelledby="headingOne"
            data-bs-parent="#accordionExample">
              <div class="accordion-body fs-6">
                <strong>This is the item's accordion body.</strong>
                Lorem ipsum dolor sit amet consectetur, adipisicing elit. Quibusdam vitae in aliquam quia quo nisi magni provident hic, ipsam, cupiditate unde! Nisi, fuga ducimus mollitia cumque dolores in hic quas!
                Alias ducimus reiciendis nisi ullam iure facilis mollitia, exercitationem sunt ut consectetur expedita aspernatur. Cupiditate vitae deserunt voluptate fuga quas tempora, fugiat accusamus, ex nemo praesentium quisquam vero, quam inventore.
              </div>
            </div>
          </div>
          <div class="accordion-item">
            <h2 class="accordion-header" id="headingTwo">
              <button class="accordion-button collapsed"
              type="button"
              data-bs-toggle="collapse"
                data-bs-target="#collapseTwo"
                aria-expanded="false"
                  aria-controls="collapseTwo">
                Nintendo Switch 官方推出紙模，善用瓦楞紙板，打造周邊配件省錢又環保
              </button>
            </h2>
            <div id="collapseTwo"
            class="accordion-collapse collapse"
              aria-labelledby="headingTwo"
              data-bs-parent="#accordionExample">
              <div class="accordion-body fs-6">
                <strong>This is the second item's accordion body.</strong>
                It is hidden by default, unti
              </div>
            </div>
          </div>
          <div class="accordion-item">
          <h2 class="accordion-header" id="headingThree">
            <button class="accordion-button collapsed"
            type="button" data-bs-toggle="collapse"
              data-bs-target="#collapseThree"
              aria-expanded="false"
              aria-controls="collapseThree">
              新版Macbook豆腐插，不但能充筆電還能充手機、平板、相機，所有配件
            </button>
          </h2>
          <div id="collapseThree"
          class="accordion-collapse collapse"
          aria-labelledby="headingThree"
          data-bs-parent="#accordionExample">
            <div class="accordion-body fs-6">
              <strong>This is the third item's accordion body.</strong>
              It is hidden by default, until th
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
      
        
    
  
</template>

<script>
export default {
  name: 'LatestNews',
  data: function () {
    return {
      flag: false

    }
  },
  methods: {
    flagClick () {
      this.flag = true
      setTimeout(()=>{
        this.flag = false
      }, 1000)
      let server = document.getElementById('server');
      /* Copy the text inside the text field */
      navigator.clipboard.writeText(server.textContent);
      /* Alert the copied text */
      // alert("Copied the text: " + server.textContent);
    },
  },
  mounted(){
    const panels = document.querySelectorAll('.panel');

    panels.forEach((panel) => {
        panel.addEventListener('click', () => {
            //remove其他active的class
            removeActiveClasses()
            //再替該panel加上active的class
            panel.classList.add('active')
        })
    })

    function removeActiveClasses() {
        panels.forEach((panel) => {
            panel.classList.remove('active')
        })
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');

.main-background{
    height: 100vh;
    background: no-repeat center url('../../assets/bg/2022-04-22_02.44.16.png');
    background-size: cover;
    display: flex;
    justify-content: center;
    align-items: center;
}
.news{
    margin-top: -90vh;
    margin-bottom: 40vh;
}
.expanding-cards{
    margin-bottom: 5vh;
}
.panel-heading .accordion-toggle:before {
    content: "－";
}
.panel-heading .accordion-toggle.collapsed:before {
    content: "＋";
}
.minecraft-banner{
  transform: scale(1);
  transition: transform 0.5s ease;
}
.minecraft-banner:hover {
  transform: scale(1.1);
  transition: transform 0.5s ease;
}
.link-box{
  background-color: #fff;
}
.pixel {
  font-family: 'VT323', monospace;
}
.copy {
  font-size: 20px;
  font-weight: 700;
  color: #fff;
}
.copy-btn{
  border: none;
}
[class*=" bi-"]::before {
  line-height: 1.1 !important;
}

.tooltip__layout {
  position: relative;
  display:inline-block;
}
.tooltip__layout:hover {
  cursor: pointer;
}

.tooltip__content.show {
   opacity:1;
   transition: 1s;
   -webkit-transition: 0.2s;
    transition: 0.2s;
}

.tooltip__content {
    padding-left: 50px;
    right:-65px;
    top:7px;
    background: #616161;
    border-radius: 2px;
    -webkit-box-shadow: 0 3px 1px -2px rgba(0,0,0,.2), 0 2px 2px 0 rgba(0,0,0,.14), 0 1px 5px 0 rgba(0,0,0,.12);
    box-shadow: 0 3px 1px -2px rgba(0,0,0,.2), 0 2px 2px 0 rgba(0,0,0,.14), 0 1px 5px 0 rgba(0,0,0,.12);
    color: #fff;
    display: inline-block;
    font-size: 12px;
    padding: 5px 8px;
    position: absolute;
    -webkit-transition: 0.2s;
    transition: 0.2s;
    width: auto;
    opacity:0;
}

.container {
	display: flex;
	/* width: 90vw; */
}

.panel {
	background-size: cover;
	background-position: center;
	background-repeat: no-repeat;
	height: 50vh;
	border-radius: 20px;
	cursor: pointer;
	flex: 0.5;
	/* 有active的class時才變寬，flex:5 */
	margin: 10px;
	position: relative; 
	/* 裡面的h3用absolute */
	transition: flex 0.4s ease-in;
	/* 展開的動畫效果 */
}

.panel:nth-of-type(1) {
  background-image: url('../../assets/bg/2022-04-22_02.45.39.png')
}
.panel:nth-of-type(2) {
  background-image: url('../../assets/bg/2022-04-22_02.33.39.png')
}
.panel:nth-of-type(3) {
  background-image: url('../../assets/bg/2022-04-22_02.44.16.png')
}
.panel:nth-of-type(4) {
  background-image: url('../../assets/bg/2022-04-22_02.32.36.png')
}
.panel:nth-of-type(5) {
  background-image: url('../../assets/bg/2022-04-22_02.49.37.png')
}

.panel h3 {
	color: #fff;
	font-size: 24px;
  text-align: start;
	position: absolute;
	bottom: 20px;
	left: 20px;
	margin: 0;
	opacity: 0;
	/* 有active的class時才opacity:1顯示文字 */
  /* display: none; */
}

.panel.active {
	/* 有active時變寬展開 */
	flex:5;
}

.panel.active h3 {
	/* 有active時顯示文字 */
  /* display: block; */
	opacity: 1;
	transition: opacity 0.3s ease-in 0.4s;
}

@media(max-width: 480px){
	.container {
		width: 100vw;
	}
	/* 螢幕太小時隱藏第4、5張圖片 */
	.panel:nth-of-type(4), .panel:nth-of-type(5) {
		display: none;
	}
}
</style>
