<script>

export default {
  name: 'Footer',
  data() {
    return {
      menuLeft: {
        title: 'Boolando s.r.l.',
        links: [
          {
            link: '#',
            text: 'Informazioni legali'
          }, {
            link: '#',
            text: 'Informativa sulla privacy'
          }, {
            link: '#',
            text: 'Diritto di recesso'
          }
        ],
      },
      menuRight: {
        title: 'Trovaci anche su',
        links: [
          {
            link: '#',
            icon: 'fa-brands fa-square-twitter'
          }, {
            link: '#',
            icon: 'fa-brands fa-square-facebook'
          }, {
            link: '#',
            icon: 'fa-brands fa-square-instagram'
          }, {
            link: '#',
            icon: 'fa-brands fa-square-pinterest'
          }, {
            link: '#',
            icon: 'fa-brands fa-square-youtube'
          }
        ]
      }
    }
  }
}

</script>

<template>

  <footer>
    <div class="container">

      <nav>
        <h3>{{ menuLeft.title }}</h3>
        <ul>
          <li 
          v-for="(item, index) in menuLeft.links" :key="index"
          >
            <a :href="item.link">
              {{ item.text }}
            </a>
          </li>
        </ul>
      </nav>

      <nav>
        <h3>{{ menuRight.title }}</h3>
        <ul>
          <li 
          v-for="(item, index) in menuRight.links" :key="index"
          >
            <a :href="item.link">
              <i :class="item.icon"></i>
            </a>
          </li>
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
  font-size: 14px;
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
