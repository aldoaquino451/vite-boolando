<script>

export default {
  name: 'Header',
  data() {
    return {
      menuLeft: [
        {
          link: '#',
          text: 'Donna'
        }, {
          link: '#',
          text: 'Uomo'
        }, {
          link: '#',
          text: 'Bmabini'
        },
      ],
      menuRight: [
        {
          link: '#',
          icon: 'fa-regular fa-user'
        }, {
          link: '#',
          icon: 'fa-regular fa-heart'
        }, {
          link: '#',
          icon: 'fa-solid fa-bag-shopping'
        }
      ]
    }
  }
}

</script>

<template>

  <header>
    <div class="container">

      <nav>
        <ul>
          <li 
          v-for="(item, index) in menuLeft" :key="index"
          >
            <a :href="item.link">
              {{ item.text }}
            </a>
          </li>
        </ul>
      </nav>
      
      <div class="image">
        <img src="../assets/img/boolean-logo.png" alt="logo">
      </div>
      
      <nav>
        <ul>
          <li 
          v-for="(item, index) in menuRight" :key="index"
          >
            <a :href="item.link">
              <i :class="item.icon"></i>
            </a>
          </li>
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
    gap: 10px;
    ul {
      height: 100%;
      list-style: none;
      display: flex;
      align-items: center;
      gap: 10px;
      a {
        text-decoration: none;
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
