<template>
<div class="container-fluid news p-5">
    <div class="row d-flex justify-content-center text-center fs-3">
      <img src="@/assets/2022.png" class='minecraft-banner mt-5 w-75' alt="">
      <div class="col col-md-4">
        <h2 class="fs-1 fw-bolder">明道場</h2>
        <h5 class="">伺服器位置</h5>
        <div class="d-flex justify-content-center">
          <div class="border px-5">
            <span class="pixel" id="server">mbc94.ntc.im</span>
          </div>
          <div class="tooltip__layout" @click="flagClick">
            <span class="ms-2"><i class="bi bi-files copy"></i></span>
            <span class="tooltip__content" :class="{'show': flag}">Copied!</span>
          </div>
        </div>
      </div>
  
      <h2 class="fs-1 fw-bolder my-5">最新消息</h2>
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
      test: 'abasdfasdfasdfc',
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
    }
  }
};
</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=VT323&display=swap');
.panel-heading .accordion-toggle:before {
    content: "－";
}
.panel-heading .accordion-toggle.collapsed:before {
    content: "＋";
}
.minecraft-banner:hover {
  transform: scale(1.1);
  transition: transform 0.5s ease;
}

.pixel {
  font-family: 'VT323', monospace;
}
.copy {
  font-size: 20px;
  color: #666;
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
</style>
