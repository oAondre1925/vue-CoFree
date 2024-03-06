<script setup>
import { ref } from 'vue'

const menuOpen = ref(false) // 控制菜单显示的响应式数据

// 切换菜单的打开状态
function toggleMenu() {
  menuOpen.value = !menuOpen.value
}

function handleAboutClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 650,
    behavior: 'smooth'
  })
}

function handleBrandClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 1300,
    behavior: 'smooth'
  })
}

function handleFeatureClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 2500,
    behavior: 'smooth'
  })
}

function handleMenuClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 4730,
    behavior: 'smooth'
  })
}

function handleProfileClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 6100,
    behavior: 'smooth'
  })
}

function handleInformationClick() {
  menuOpen.value = false
  window.scrollTo({
    top: 6600,
    behavior: 'smooth'
  })
}

</script>

<template>
  <div class="header">
    <div class="header_container">
      <div class="header_logo">
        <img src="./assets/logo.png" height="100px" width="100px">
      </div>
      <div class="header_menu">
        <p @click="toggleMenu">● Menu</p>
        <div :class="{'menuBar':true, 'menuBar-open': menuOpen }">
          <span @click="toggleMenu" class="closeMenu">🗙Close</span>
          <ul :class="{ 'menu':true, 'menu-visible': menuOpen }">
            <li><a @click="handleAboutClick">About</a></li>
            <li><a @click="handleBrandClick">Brand</a></li>
            <li><a @click="handleFeatureClick">Feature</a></li>
            <li><a @click="handleMenuClick">Menu</a></li>
            <li><a @click="handleProfileClick">Profile</a></li>
            <li><a @click="handleInformationClick">Information</a></li>
            <div class="menuBar_content">
              <p>(02)22151234<br>平日:10:30〜20:30 週六10:30〜18:30 週日店休
                <br>歡迎來電預約，也可以在FB、Instagram與我們聯絡!</p>
            </div>
          </ul>
        </div>
      </div>
    </div>
  </div>

  <div class="home_container">
            <div class="home_photo">
                <img src="./assets/cover_photo.png" style="width: 680px;height: 620px;">
            </div>
            <div class="home_slogon">
                <h4>優雅的享受唇邊的馨香☕</h4>
                <p>Whether you seek solace in a quiet corner or engage in heartfelt conversations <br>with kindred spirits.
                    A journey into the realm of exquisite coffee flavors and <br>serene moments. </p>
            </div>
        </div>
</template>

<style land="scss" scoped>
  .header{
    width: 100%;
    height: auto;
    background-color: #ffffff80;
    backdrop-filter: blur(10px);
    opacity: 1;
    z-index: 100;
    display: flex;
    position: fixed;
    top:0;
  }
  .header_container{
    width: 100%;
    height: auto;
    display: flex;
    justify-content: space-between;
  }
  .header_logo{
    display: flex;
    cursor: pointer;
  }
  .header_menu{
    display: flex;
    padding: 1rem;
    background-color: transparent;
    align-items: center;
  }
  .header_menu p{
    padding: 0px 30px;
    font-size: 20px;
    font-weight: 600;
    font-family: New Century Schoolbook, TeX Gyre Schola, serif;
    color: rgb(68, 68, 67);
    cursor: pointer;
  }

  .closeMenu{
    color: aliceblue;
    font-size: 20px;
    font-weight: 600;
    transition: .2s;
    position: fixed; /* Changed from absolute to fixed */
    top: 28px; /* Position it towards the top of the viewport */
    right: 48px;
    display: none;
}
.closeMenu:hover{
  color: rgb(159, 159, 159);
  cursor: pointer;
}

.menu{
  display: flex;
  flex-direction: column;
  position: absolute;
  top: 45%;
  left: 50%;
  transform: translate(-50%,-50%);
  opacity: 0;
  transition: all 0.3s ease;
  cursor: pointer;
  li{
    list-style: none;
    a{
      display:block;
      text-decoration: none;
      font-size: 1.2rem;
      transition:0.1s ease-in;
      color: antiquewhite;
      font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
      &:hover{
        color: inherit;
      }
    }
  }
}

.menuBar{
  position: fixed;
  top: -100vh; /* 初始為視圖之外，保持隱藏 */
  left: 0px;
  width: 100%;
  height: 100vh;
  background-color: #303436;
  transition: top 0.3s ease-in;
  text-align: center;
  z-index: 100;
}
.menuBar_content{
  p{
    cursor:default;
    color: antiquewhite;
    font-size: 1rem;
    font-family: sans-serif;
    font-weight: 600;
  }
}
.menuBar-open {
  top: 0;
}

.menu-visible {
  opacity: 1;
}
.menuBar-open .closeMenu {
  display: block;
}

   /*封面*/
  .home_container{ 
    margin-top: 136px;
    display: flex;
    justify-content: center;
    align-items: center;
  }
  .home_photo{
    overflow: hidden;
    justify-content: center;
  }

  .home_slogon{
    max-width:100%;
    height: auto;
    h4{
      width: 27px;
      height: auto;
      font-size: 22px;
      text-align: left;
      margin: auto;
      padding-bottom: 50px;
    }
    p{
      font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
      font-weight: 600;
      font-size: 14px;
      padding-top: 50px;
      text-align: left;
      max-width: 60%;
      height:auto;
      margin: auto;
      color: rgb(23, 23, 23);
    }
  }

@media only screen and (max-width:900px){ /*RWD : 900px*/
  /*side bar*/
  .menuBar_content{
    padding: 0;
    p{
      font-size: 1rem;
    }
  }
  #menuBar{
    position: fixed;
    top: -1000%;
    left: 0;
    width:100%;
    height: 1000%;
    background-color: #303436;
    transition: 0.3s ease-in;
    text-align: center;
}
#menu li a{
  width: 100%;
  height: auto;
}
#closeMenu{
    color: aliceblue;
    font-size: 2.5vw;
    font-weight: 600;
    transition: .2s;
    position: fixed; /* Changed from absolute to fixed */
    top: 28px; /* Position it towards the top of the viewport */
    right: 48px;
    display: none;
  }
}

@media only screen and (max-width:768px){   /*   RWD: 768px */
  .home_container{
    flex-direction: column-reverse;
    align-items: center;
    justify-content: end;
  }
  .home_photo{
    max-width: 100%;
    height: auto;
  }
  .home_slogon{
    width: 100%;
    padding-bottom:2rem ;
  }
/*side bar*/
#menu{
  top: 40%;
  left: 50%;
  transform: translate(-50%,-50%);
  cursor: pointer;
}
#menuBar{
  position: fixed;
  top: -120vh; /* 初始為視圖之外，保持隱藏 */
  left: 0;
  width: 100%;
  height: 120vh;
  background-color: #303436;
  transition: top 0.3s ease-in;
  text-align: center;
  z-index: 100;
}
.menuBar_content{
  padding: 0;
  width: 100%;
  height: auto;
  p{
    font-size: 1rem;
  }
}
#closeMenu{
    color: aliceblue;
    font-size: 3.8vw;
    font-weight: 600;
    transition: .2s;
    position: fixed; /* Changed from absolute to fixed */
    top: 28px; /* Position it towards the top of the viewport */
    right: 48px;
    display: none;
  }
}
</style>
