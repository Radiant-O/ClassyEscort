<script lang="ts" setup>
import top from "./components/top.vue";
import Home from "./views/Home.vue";
import SignIn from "./views/SignIn.vue";
import apage from "./views/pages/a.vue"
</script>

<template>
  <main class="real">
    <top />
    
    <body>
      <RouterView/>
    </body>
    <!-- <Home/> -->
    <!-- <apage/> -->
  </main>
</template>

<style>
</style>
