<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const goTopVisible = ref(false); 

const handleScroll = () => {
  const currentScroll = window.scrollY || document.documentElement.scrollTop;
  goTopVisible.value = currentScroll > lastScrollTop && currentScroll > originalPosition;
  lastScrollTop = currentScroll <= 0 ? 0 : currentScroll;
};

let lastScrollTop = 0;
let originalPosition;

onMounted(() => {
  originalPosition = document.documentElement.scrollTop;
  window.addEventListener('scroll', handleScroll);
  handleScroll(); 
});

onUnmounted(() => {
  window.removeEventListener('scroll', handleScroll);
});

const scrollToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: 'smooth'
  });
};
</script>

<template>
  <button class="goTop" @click="scrollToTop" v-if="goTopVisible">⌅</button>
</template>

<style lang="scss" scoped>
.goTop {
  position: fixed;
  bottom: 30px;
  right: 40px;
  transition: transform 1s ease, opacity 0.5s;
  transform: translateY(0);
  opacity: 0.6;
  display: flex;
  justify-content: center;
  align-items: center;
  width: 6vh;
  height: 6vh;
  font-size: 2.5rem;
  border: none;
  border-radius: 5px;
  background-color: rgba(255, 255, 255, 0);
  margin-left: auto;

  &:hover {
    color: #515151;
  }
}
</style>
