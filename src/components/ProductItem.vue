<template>
  <div class="mainText">
    <div class="block" v-for="cls in data">
      <div class="img">
        <img class="productsImg" :src="cls.img" alt="" />
      </div>
      <div class="information">
        <h2>{{ cls.title }}</h2>
        <p>{{ cls.date }}</p>
        <p>{{ cls.address }}</p>
        <p>{{ cls.information }}</p>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
        <i class="bi bi-star-fill"></i>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      data: [
        {
          id: 1,
          img: require("../assets/products/sticker.jpg"),
          title: "麥塊競賽貼紙",
          information:
            "1. 初選-麥塊競賽貼紙 2. 挑戰賽-麥塊競賽貼紙 3. 邀請賽-麥塊競賽貼紙 4. 競賽口罩-麥塊競賽貼紙",
        },
        {
          id: 2,
          img: require("../assets/products/storageBag.jpg"),
          title: "文大場-參與獎",
          information:
            "防撥水毛氈布收納包",
        },
        {
          id: 3,
          img: require("../assets/products/keyRing.jpg"),
          title: "明道場-參與獎",
          information:
            "雷雕特製鑰匙圈示意圖",
        },
        {
          id: 4,
          img: require("../assets/products/BeverageBag.jpg"),
          title: "北護場-參與獎",
          information:
            "手工筆袋、飲料提袋",
        },
        {
          id: 5,
          img: require("../assets/products/keyRing2.jpg"),
          title: "真理場-參與獎",
          information:
            "特製鑰匙圈",
        },
      ],
    };
  },
};
</script>

<style scoped>
#carouselExampleDark {
  margin-bottom: 20px;
}
.d-block {
  height: 500px;
}
.carousel-control-prev-icon,
.carousel-control-next-icon {
  border: solid 1px white;
  border-radius: 50%;
}
.mainText {
  margin-left: auto;
  margin-right: auto;
  max-width: 1200px;
}
.block {
  padding: 20px;
  margin: 60px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
  border-radius: 8px;
}
.block:hover {
        cursor: pointer;
        transform: scale(1.05);
        transition: transform 0.5s ease;
    }
.productsImg {
  max-width: 400px;
  max-height: 250px;
}
.img,
.information {
  display: inline-block;
  width: 50%;
}
.information {
  vertical-align: middle;
}
@media screen and (max-width: 1100px) {
  #carouselExampleDark {
    display: none;
  }
  h1 {
    text-align: center;
  }
  hr {
    width: 60%;
    margin-left: auto;
    margin-right: auto;
  }
  .block {
    max-width: 500px;
    margin-left: auto;
    margin-right: auto;
    margin-top: 30px;
  }
  .img,
  .information {
    margin-bottom: 10px;
    display: inline-block;
    width: 100%;
  }
  .productsImg {
    width: 100%;
  }
}
.bi-star-fill {
    color: rgb(255, 208, 0);
    }
</style>
