<template>
  <div class="col-12 col-md-4">
    <div class="card">
        <div class="item-img">
          <img :src="images" class="card-img-top" alt="...">
        </div>
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
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ProductItem',
  data() {
    return {
      images: require('../assets/Frog_1.png'),
    };
  },
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
.card {
        box-shadow: 0 0 10px rgba(0, 0, 0, 0.2);
    }
    .card:hover {
        cursor: pointer;
        transform: scale(1.1);
        transition: transform 0.5s ease;
    }
    /* .item-img{
        width: 100%;
    } */
    .card-img-top{
        width: 100%;
        height: 20rem;
        object-fit:  scale-down;
    }

    .bi-star-fill {
    color: rgb(255, 208, 0);
    }

</style>
