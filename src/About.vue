<script setup>
import { ref, onMounted, onUnmounted } from 'vue';

const observedElements = ref([]);

const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry) => {
    if (entry.isIntersecting) {

      entry.target.classList.add('show');
    } else {
      entry.target.classList.remove('show');
    }
  });
});

onMounted(() => {
  observedElements.value = document.querySelectorAll('.scrollUp');
  observedElements.value.forEach(el => observer.observe(el));
});

onUnmounted(() => {
  observedElements.value.forEach(el => observer.unobserve(el));
});
</script>


<template>
    <div class="about">
      <div class="about_us">
        <img src="./assets/about.png" class="scrollUp">
        <h4 class="scrollUp" style="padding: 1rem;">About Us</h4>
        <p class="scrollUp">寧靜的空間與濃郁的咖啡相伴，為您締造一片悠然自得的小天地。</p>
      </div>
    </div>
  </template>

<style lang="scss" scoped>
  /* 關於我們 */
  .about{
    display: flex;
    justify-content: center;
  }
  .about_us{
    text-align: center;
    img{
        max-width:50% ;
        height: auto;
        transform: translateY(20%);
        transition: transform 1s linear;
        opacity: 0;
        margin-top: -4px;
    }
    h4{
        font-size: 1.5rem;
        transform: translateY(10%);
        transition: transform 1s linear;
        opacity: 0;
        margin: auto;
    }
    p{
        font-size: 1rem;
        transform: translateY(10%);
        transition: transform 1s linear;
        opacity: 0;
        font-weight: 600;
        padding-bottom: 2rem;
        margin: auto;
    }
  }

.scrollUp.show {
  opacity: 1;
  transform: translateY(0);
}
  @media only screen and (max-width:767px){ /*RWD : 900px*/
    .about_us img{
      max-width: 100%;
      height: auto;
    }
  }
</style>
