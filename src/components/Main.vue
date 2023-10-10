<script>

export default {
  name: 'Main',
  data() {
    return {
      cards: [
        {
          imgFirst: '1.webp',
          imgSecond: '1b.webp',
          imgName: 'levi\'s',
          discount: '-40%',
          eco: 'sostenibilità',
          productBrand: 'Levi\'s',
          productName: 'Relaxed fit tee Unisex',
          productPrice: '29,99',
          productDiscounted: '14,99'
        }
      ]
    }
  }
}

</script>

<template>

  <main>
    <div class="container-sm">
      <div class="cards">

        <div class="card">

          <div class="card-image">
            <img src="../assets/img/1.webp" alt="levi's">
            <img src="./img/1.webp" alt="levi's">
            <div class="card-image-heart">
              <span class="heart"><i class="fa-solid fa-heart"></i></span>
              <span class="heart"><i class="fa-regular fa-heart"></i></span>
            </div>
            <div class="card-image-content">
              <span>-50%</span>
              <span>Sostenibilità</span>
            </div>
          </div>

          <div class="card-product">
            <p class="product-brand">Levi's</p>
            <p class="product-name"><b>Relaxed fit tee Unisex</b></p>
            <p class="product-price"><b>14,99 &euro;</b> <span>29,99 &euro;</span></p>
          </div>

        </div>

        <div class="card">card</div>  
        <div class="card">card</div>  
        <div class="card">card</div>  
        <div class="card">card</div>  
        <div class="card">card</div>  
      </div>
    </div>
  </main>
  
</template>

<style lang="scss">

@use '../scss/partials/variabiles' as *;

main {
  .cards {
    margin: 50px 0;
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 15px;
    .card {
      width: 250px;
      min-height: 200px;
      border: 1px solid black;
    }
  }
}

</style>
