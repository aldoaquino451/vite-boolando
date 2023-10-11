<script>

export default {
  name: 'Card',
  props: {
    firstImage: String,
    secondImage: String,
    discount: String,
    eco: Boolean,
    brand: String,
    type: String,
    firstPrice: Number,
    lastPrice: Number,
  }
}

</script>

<template>

  <div class="card">
    <div class="card-top">
      <div class="product images">
        <img 
          class="main" 
          :src="`../assets/img/${firstImage}`" 
          :alt="brand"
        >
        <img 
          class="alternative" 
          src="../assets/img/1b.webp" 
          :alt="brand"
        >
      </div>
      <div class="product heart">
        <span><i class="fa-regular fa-heart"></i></span>
      </div>
      <div class="product info">
        <span class="content discount" v-if="discount">{{ discount }}</span>
        <span class="content eco" v-if="eco">Sostenibilità</span>
      </div>
    </div>

    <div class="card-bottom">
      <span class="brand">
        {{ brand }}
      </span>
      <span class="type">
        {{ type }}
      </span>
      <span class="price">
        <span 
          v-if="firstPrice"
        >&euro; {{ firstPrice }}
        </span>
        <span 
          class="discount" 
          v-if="lastPrice"
        >&euro; {{ lastPrice }}
        </span>
      </span>
    </div>
  </div>

</template>

<style lang="scss" scoped>

@import '../scss/partials/variabiles' ;

.card {
  width: 300px;
  display: flex;
  flex-direction: column;
  gap: 8px;
  margin-bottom: 20px;
  img {
    width: 100%;
  }

  .card-top {
    width: 100%;
    position: relative;
    .images {
      width: 100%;
      position: relative;
      .alternative {
        display: none;
      }
      &:hover .alternative {
        position: absolute;
        top: 0;
        left: 0;
        display: inline-block;
      }
    }
    .heart {
      position: absolute;
      right: 10px;
      top: 10px;
      background-color: $text-h-f-color;
      width: 40px;
      height: 40px;
      display: flex;
      justify-content: center;
      align-items: center;
      &:hover i {
        color: $discount-color;
      }
    }
    .info {
      position: absolute;
      bottom: 25px;
      left: 0;
      color: $text-h-f-color;
      .content {
        padding: 5px 10px;
        &.discount {
          background-color: $discount-color;
          margin-right: 10px;
        }
        &.eco {
          background-color: $eco-color;
        }
      }
    }
  }
  .card-bottom {
    display: flex;
    flex-direction: column;
    gap: 4px;
    .brand {
      font-size: 0.9rem;
    }
    .type {
      font-weight: bold;
    }
    .price {
      color: $discount-color;
      font-weight: bold;
      display: flex;
      gap: 10px;
      .discount {
        color: $text-m-color;
        text-decoration: line-through;
        font-weight: normal;
      }
    }
  }
}
  
</style>