<template>
<div class="container-fluid news p-5">
    <div class="row d-flex justify-content-center text-center fs-3">
    <h2 class="display-3 fw-bold mb-5 mt-5">最新消息</h2>
        <div class="col col-md-10 col-lg-10 accordion" id="accordionExample">
  <div class=" accordion-item">
    <h2 class="accordion-header" id="headingOne">
      <button class="accordion-button"
      type="button"
       data-bs-toggle="collapse"
        data-bs-target="#collapseOne"
         aria-expanded="true"
         aria-controls="collapseOne">
        [開箱]Google Home 智慧喇叭音質更好，可控制更多智能設備，讓居家變得更智慧
      </button>
    </h2>
    <div id="collapseOne"
     class="accordion-collapse collapse show"
      aria-labelledby="headingOne"
       data-bs-parent="#accordionExample">
      <div class="accordion-body">
        <strong>This is the first item's accordion body.</strong> It is shown by default, unti
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
      <div class="accordion-body">
        <strong>This is the second item's accordion body.</strong> It is hidden by default, unti
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
      <div class="accordion-body">
        <strong>This is the third item's accordion body.</strong> It is hidden by default, until th
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
};
</script>

<style scoped>
.panel-heading .accordion-toggle:before {
    content: "－";
}
.panel-heading .accordion-toggle.collapsed:before {
    content: "＋";
}
</style>
