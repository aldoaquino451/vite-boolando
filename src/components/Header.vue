<script>

export default {
  name: 'Header',

}

</script>

<template>

  <header>
    <div class="container">

      <nav>
        <ul>
          <li>icona</li>
          <li>icona</li>
          <li>icona</li>
        </ul>
      </nav>
      
      <div class="image">
        <img src="../assets/img/boolean-logo.png" alt="logo">
      </div>
      
      <nav>
        <ul>
          <li>icona</li>
          <li>icona</li>
          <li>icona</li>
        </ul>
      </nav>

    </div>
  </header>
  
</template>

<style lang="scss">

@use '../scss/partials/variabiles' as *;

header {
  background-color: $header-color;
  color: $text-h-f-color;
  padding: 10px 0;
  .container {
    display: flex;
    justify-content: space-between;
    ul {
      height: 100%;
      list-style: none;
      display: flex;
      align-items: center;
      gap: 10px;
      li {
        color: $text-h-f-color;
      }
    }
    .image {
      height: 30px;
      img {
        height: 100%;
      }
    }
  }
}

</style>
