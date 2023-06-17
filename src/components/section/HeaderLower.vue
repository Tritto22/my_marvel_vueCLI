<template>
  <div class="header-lower">
    <nav>
      <ul class="navbar d-flex justify-content-center">
        <li v-for="(link, i) in headerLowerLinks" :key="i">
          <a :href="link.link" class="text-uppercase fw-bold text-decoration-none">{{link.name}}</a>
        </li>
      </ul>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'HeaderLower',
  data() {
    return {
      headerLowerLinks: [
        {
          name: 'news',
          link: '#'
        },
        {
          name: 'comics',
          link: '#'
        },
        {
          name: 'characters',
          link: '#'
        },
        {
          name: 'movies',
          link: '#'
        },
        {
          name: 'tv shows',
          link: '#'
        },
        {
          name: 'games',
          link: '#'
        },
        {
          name: 'videos',
          link: '#'
        },
        {
          name: 'more',
          link: '#'
        }
      ]
    };
  }
}
  
</script>

<style lang="scss" scoped>
@import 'bootstrap';
@import '../../assets/style/partials/variables.scss';
  .header-lower{
    max-width: 1200px;
    margin: auto;
    .navbar{
      li{
        text-transform: uppercase;
        padding: 0 18px;
        cursor: pointer;
        list-style: none;
        a{
          color: $primary-txt-color-light;
          font-size: $lower-font-size;
        }
      }
      
    }

  }

</style>