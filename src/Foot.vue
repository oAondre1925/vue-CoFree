<script setup>

</script>

<template>
<div class="foot">
    <div class="foot_img"><img src="./assets/certififed.png" style="max-width: 100%;height: auto;"></div>
    <div class="foot_content"><p>「此網站無任何商業用途」<br>
        網頁風格參考 <a href="https://yohaku.salon/">Yohaku</a>，圖片來源由ChatGPT、
    <a href="https://www.freepik.com/icon/soup_619242#fromView=resource_detail&position=62">FREEPIK</a>提供。</p>
    </div>
</div>
<div class="foot_bottom">
    <p>©︎2024 & CoFree </p>
    <div class="foot_svg">
        <i class="instagram"><img src="./assets/instagram.svg" ></i>
        <i class="facebook"><img src="./assets/facebook.svg"></i>
        <i class="email"><img src="./assets/email.svg"></i>
    </div>
</div>
</template>

<style lang="scss">
/*Foot*/
.foot{
    display: flex;
    align-items: center;
    flex-direction: column;
    padding: 5rem 22rem;
  }
  .foot_img{
    width: 150px;
    height: auto;
    padding-bottom: 20px;
  }
  .foot_content{
    width: 500px;
    height: auto;
    p{
      font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
      line-height: 2;
      font-size: 16px;
      font-weight: 600;
      text-align: center;
    }
    a{
      color: #4f4036;
    }
  }
  .foot_bottom{
    display: flex;
    padding: 3rem 5rem;
    p{
      font-size: 14px;
      font-weight: 600;
      font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    }
  }
  .foot_svg{
    padding: 0 1rem;
    vertical-align: top;
    align-items: center;
    cursor: pointer;
  i{
    padding: 0 5px;
  }
}
  @media only screen and (max-width:900px){ /*RWD : 900px*/
    .foot_img{
      width: 120px;
      height: auto;
      padding-bottom: 10px;
    }
    .foot_content p{
      font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
      line-height: 2;
      font-size: 1rem;
      font-weight: 600;
    }
  }
  @media only screen and (max-width:767px){   /*   RWD: 767px */
/*Foot*/
.foot{
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;

  padding:4rem 0;
}
.foot_img{
  width: 100px;
  height: auto;
  padding-bottom: 20px;
}
.foot_content{
  width: 300px;
  height: auto;
  p{
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    line-height: 2;
    font-size: 3vw;
    font-weight: 600;
    text-align: center;
  }
}

.foot_bottom{
  display: flex;
  justify-content: start;
  padding: 0;
  p{
    font-size:1rem;
    font-weight: 600;
    font-family:'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
}
.foot_svg{
  padding: 0 1rem;
  vertical-align: top;
  cursor: pointer;
  i{
    padding: 0 5px;
  }
}
/*Foot*/
}
</style>
