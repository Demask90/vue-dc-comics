<template>
  <header>
    <div class="w-60 flex between middle">
      <a href="/">
        <img alt="Vue logo" src="@/assets/img/dc-logo.png">
      </a>

      <nav>
        <ul class="flex">
          <li v-for="(link, index) in links" :key="index">
            <a :class="(link.current) ? 'active' : null" :href="link.url">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
    </div>
  </header>
</template>

<script>
import Links from '@/assets/data/Links.js';
export default {
  name: 'Header',

  data() {
    return {
      links: Links.headerLinks,
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
  @import "../style/vars";

  header {
    padding: 5px 0;
    width: 100%;
    margin: 0 auto;

    img {
      width: 80%;
    }

    ul {
      list-style: none;
      flex-direction: row;
      
      li a {
        display: inline-block;
        padding: 1rem;
        text-decoration: none;
        font-weight: 500;
        transition: color 0.3s;

        &:hover,
        &.active {
          color: $primary;
        }
      }
    }
  }
</style>
 