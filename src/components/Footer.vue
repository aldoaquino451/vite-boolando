<script>

export default {
  name: 'Footer',

}

</script>

<template>

  <footer>
    <div class="container">

      <nav>
        <h3>titolo</h3>
        <ul>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
        </ul>
      </nav>

      <nav>
        <h3>titolo</h3>
        <ul>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
          <li><a href="#">link</a></li>
        </ul>   
      </nav>

    </div>
  </footer>
  
</template>

<style lang="scss">

@use '../scss/partials/variabiles' as *;

footer {
  background-color: $footer-color;
  color: $text-h-f-color;
  padding: 20px 0;
  .container {
    display: flex;
    justify-content: space-between;
    h3 {
      margin-bottom: 20px;
    }
    ul {
      list-style: none;
      display: flex;
      gap: 10px;
      a { 
        text-decoration: none;
        color: $text-h-f-color;
      } 
    }
  }
}
</style>
