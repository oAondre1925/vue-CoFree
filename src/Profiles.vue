<script setup>

</script>

<template>
<div class="profile">
  <div class="profile_img"><img src="./assets/profile.png" style="max-width:100%;height:85%;border-radius: 5px;"></div>
      <div class="profile_item">
          <p id="profile">Profile</p>
          <p id="name">Chen  <span>Andre</span></p>
          <p id="introduction">出生於2000年，我畢業於私立銘傳大學資訊傳播工程學系。本網站採用單頁式應用程式（SPA）設計，並實現了響應式網頁設計（RWD）以達到各種裝置的最佳瀏覽體驗。在網頁排版上，我運用Flex Box的單向排版系統和Grid的雙向排版系統作為基礎，以創造出整潔且易於導航的用戶介面。
          </p>
      </div>
</div>
</template>

<style lang="scss">
.profile{
    display: flex;
    flex-direction: row;
    justify-content: center;
    align-items: center;
    background-color:#faf7f7;
    max-width: 100%;
    height: auto;
  }
  .profile_img{
    display: flex;
    align-items: center;
    width: 300px;
    height:300px;
    margin: 50px 50px;
  }
  .profile_item{
    display: flex;
    flex-direction: column;
    max-width: 50%;
    height: auto;
  }
  #profile{
    font-size: 1.5rem;
    box-shadow: 0 1.5px 0px rgb(74, 74, 74);
    max-width: 12%;
    height: auto;
    padding: 5px 0;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  }
  #name{
    font-size: 1.5rem;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    color: #3b3a3a;
    span{
      font-size: 1.2rem;
      font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
      padding-left: 10px;
      color: #3b3a3a;
    }
  }
  #introduction{
    font-size: 1rem;
    font-weight: 600;
    line-height: 1.5;
    text-align: left;
    font-family: sans-serif;
  }
  @media only screen and (max-width:767px){ /*RWD : 900px*/
/*自我介紹*/
.profile{
  display: flex;
  flex-direction:column;
  justify-content: center;
  align-items: center;
  background-color:#faf7f7;
  max-width: 100%;
  height: auto;
}
.profile_img{
  display: flex;
  align-items: center;
  width: 300px;
  height:300px;
  margin:0;
}
.profile_item{
  max-width: 80%;
  height: auto;
}
#profile{
  font-size: 1.4rem;
  box-shadow: 0 0 0px rgb(74, 74, 74);
  max-width: 100%;
  height: auto;
  padding:0;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
}
#name{
  font-size: 1.2rem;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  color: #3b3a3a;
  span{
    font-size: 1.1rem;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    padding-left: 10px;
    color: #515151;
  }
}
#introduction{
  font-size: 1rem;
  font-weight: 600;
  line-height: 1.5;
  text-align: left;
  font-family: sans-serif;
  font-size: 0.75rem;
}
/*自我介紹*/
}
</style>
