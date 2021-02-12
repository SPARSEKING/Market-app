<template>
  <header>
    <div class="navbar">
      <div class="container">
        <div class="navbar-content">
          <div class="logo">MARKET-APP</div>
          <ul class="navbar-list">
            <li class="navbar-item" v-for="link in links" :key="link.title">
              <router-link class="navbar-link" :to="link.url">{{
                link.title
              }}</router-link>
            </li>
          </ul>
        </div>
      </div>
    </div>
  </header>
  <router-view />
</template>

<script lang="ts">
import { defineComponent } from "vue";

export default defineComponent({
  name: "App",
  data() {
    return {
      links: [
        {
          title: "Home",
          url: "/"
        },
        {
          title: "About",
          url: "/about"
        }
      ]
    }
  }
});
</script>

<style scoped>
.router-link-exact-active {
  color: #5247e7;
}
</style>


