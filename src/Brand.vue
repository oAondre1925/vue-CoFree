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
  <div class="brand" >
            <div class="brand_container">
                <div class="brand_img">
                    <img src="./assets/brand-story.png" class="scrollUp"  id="brand_st">
                    <img src="./assets/brand-story02.png"  class="scrollUp" id="brand_nd">
                </div>
                <div class="brand_content" >
                    <h5  class="scrollUp" style="font-size: 26px;padding: 10px;">Brand Story</h5>
                    <p class="scrollUp" >咖啡不僅僅是一種飲品，它是情感與回憶的載體。在每一滴經典的咖啡中，
                        我們看到了不同文化的交融與人心的聯繫。這是一場味覺與心靈的旅行，每一口都盛載著故事和溫度。</p>
                    <p class="scrollUp" >我們提供的是一個故事，一段旅程。每顆咖啡豆都來自遠方的土地，它們的旅程從農場到杯中，每一步
                        都充滿了對品質和可持續性的堅持。</p>
                    <p class="scrollUp" >每個角落都講述著一個關於咖啡的故事。這是一個人們可以聚集、交流、分享生活點滴的場所。我們相信，咖啡的魅力在於它能將人們緊緊相連。</p>
                </div>
            </div>
        </div>
</template>

<style lang="scss">
.brand{
    background-color:#faf7f7;
    padding: 2rem 8rem ;
  }
  .brand_container{
    display: flex;
    justify-content: start;
    width:100%;
    height: auto;
  }
  .brand_img{
    margin: 1rem;
    img{
        width: 380px;
        height: 300px;
        display: flex;
        vertical-align: top;
        transform: translateY(20%);
        transition: transform 1s linear;
        animation: fade 1s linear ;
        opacity: 0;
    }
  }
  .brand_content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    margin-bottom: 6rem;
    max-width: 50%;
    height: auto;
  }
  .brand_content h5,.brand-content p{
    font-size: 1.2vw;
    text-align: left;
    transform: translateY(60%);
    transition: transform 1s linear;
    animation: fade 1.5s linear ;
    opacity: 0;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .brand_content p{
    padding: 2rem 0;
    font-weight: 600;
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  }
  .scrollUp.show {
  opacity: 1;
  transform: translateY(0);
}
  @media only screen and (max-width:900px){
    .brand{
      background-color:#faf7f7;
      padding:0;
    }
    .brand_container{
      width: 100%;
      height: auto;
    }
    .brand_img img{
      width: 350px;
      height: 300px;
      margin-right: 1rem;
      vertical-align: top;
    }
  }

  @media only screen and (max-width:767px){   /*   RWD: 767px */
  .brand_container{
    flex-direction: column;
    width: 100%;
    text-align: center;
    overflow: auto; 
    word-wrap: break-word;
  }
  .brand_img{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    img{
        width: 100%;
        height: auto;
        padding: 0;
    }
  }
  #brand_st{
    position:relative;
    width: 80%;
    height:180px;
  }
  #brand_nd{
    width: 173px;
    height: 105px;
    position: absolute;
    margin-left: 210px;
    margin-top: 120px;
  }
  .brand_content{
    max-width: 100%;
    height: auto;
    margin:auto;
    text-align: center;
    padding: 1rem;
    h5{
        text-align: center;
    }
  }
}
</style>
