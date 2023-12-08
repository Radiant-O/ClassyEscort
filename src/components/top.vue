<template>
  <header class="top">
    <div class="top_menu">
      <div class="logo">
        <img class="w-[5rem] lg:w-[10rem]" src="../assets/images/classy.png" alt="" />
      </div>
      
      <nav class="nav">
        <router-link to="/escorts">ESCORTS</router-link>
        <router-link to="/reviews">REVIEWS</router-link>
        <router-link to="/about">ABOUT</router-link>
        <router-link to="/contact-us">CONTACT US</router-link>
      </nav>

      <div class="lg:hidden sm:block" @click="toggleNav">
        <AlignRightOutlined class="menu_bar" />
      </div>
    </div>
    
  </header>
  <monav v-if="nav"/>
</template>

<script setup>
import monav from "./monav.vue";
import { ref } from "vue";
import { AlignRightOutlined } from "@ant-design/icons-vue";
const nav = ref(false);

const toggleNav = () => {
  nav.value = !nav.value;
};
</script>

<style>
.slide-menu-enter-active {
  transform: translate(0, 0);
  -webkit-transform: translate(0, 0);
  transform: translate(275px, 0);
  -webkit-transform: translate(275px, 0);
}

.slide-menu-leave-active {
  transform: translate(275px, 0);
  -webkit-transform: translate(275px, 0);
}
</style>
