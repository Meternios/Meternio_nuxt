<script setup>
import { ref } from 'vue';

const year = ref(new Date().getFullYear());
</script>

<template>
  <footer class="footer bg-gray text-white relative z-50">
    <div class="footer-container container flex items-center justify-between py-5">
      <p class="footer-copyright m-0">{{ $t("footer.copyright", {year: year}) }}</p>
      <div class="footer-socials flex">
        <a href="https://www.instagram.com/meternio/" target="_blank" class="mr-2"
          ><Icon name="fa6-brands:instagram" /></a>
        <NuxtLink :to="localePath('/contact')" :aria-label="$t('footer.contact')" class="header-logo"><Icon name="fa6-regular:envelope" class="mr-2"/></NuxtLink>
        <a href="https://wa.me/41762047832" target="_blank" class="mr-2"
          ><Icon name="fa6-brands:whatsapp" /></a>
        <a href="https://github.com/meternios" target="_blank"
          ><Icon name="fa6-brands:github" /></a>
      </div>
    </div>
  </footer>
</template>
