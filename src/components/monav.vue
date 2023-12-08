<template>
  <transition name="slide-menu">
    <section class="monav" v-if="!nav">
      <nav class="mob_nav">
        <!-- <CloseOutlined class="close_btn" @click="toggleNav" /> -->

        <div><router-link to="/escorts">ESCORTS</router-link></div>
        <div><router-link to="/reviews">REVIEWS</router-link></div>
        <div><router-link to="/about">ABOUT</router-link></div>
        <div><router-link to="/contact-us">CONTACT US</router-link></div>
      </nav>
    </section>
  </transition>
</template>

<script setup>
import { CloseOutlined } from "@ant-design/icons-vue";

import { ref } from "vue";
const nav = ref(false);

const toggleNav = () => {
  nav.value = !nav.value;
};
</script>
