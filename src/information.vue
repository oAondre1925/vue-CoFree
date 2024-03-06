<script setup>

</script>

<template>
<div class="information">
    <div class="information_pic">
        <div id="carouselExampleIndicators" class="carousel slide carousel-fade"data-bs-ride="carousel">
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="1" aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="2" aria-label="Slide 3"></button>
                <button type="button" data-bs-target="#carouselExampleIndicators" data-bs-slide-to="3" aria-label="Slide 4"></button>
            </div>
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <img src="./assets/envirment.png" class="  ">
                    </div>
                    <div class="carousel-item">
                      <img src="./assets/envirment1.png" class=" ">
                    </div>
                    <div class="carousel-item">
                      <img src="./assets/envirment2.png" class="">
                    </div>
                    <div class="carousel-item">
                      <img src="./assets/envirment3.png" class=" ">
                    </div>
                </div>
        </div>
    </div>
        <div class="information_container">
            <div class="information_content">
                <h4>Information</h4>
                <table>
                    <tr>
                        <th>Adress</th>
                        <td>天龍國阿貓市阿狗街24-1F</td>
                    </tr>
                    <tr>
                        <th>Open</th>
                        <td>平日:10:30〜20:30 <br>週六10:30〜18:30</td>
                    </tr>
                    <tr>
                        <th>Closed</th>
                        <td>星期日</td>
                    </tr>
                    <tr>
                        <th>Contact</th>
                        <td>(02)22151234<br>animalcute123@gmail.com</td>
                    </tr>
                    <tr>
                        <th>Reserve</th>
                        <td>歡迎來電預約，也可以在FB、Instagram與我們聯絡!</td>
                    </tr>
                </table>
            </div>
        </div>
</div>
</template>

<style lang="scss">
  /*information area*/
  .information{
    display: flex;
    justify-content: center;
  } 
  .information_pic{  
    width:500px;
    height: auto;
    padding: 4rem 2rem;
  }
  .information_container{
    max-width: 100%;
    height: auto;
    display: grid;
    margin: 0 5rem;
    line-height: 2;
  }
  .information_content{
    display: flex;
    flex-direction: column;
    justify-content: center;
    max-width: 100%;
    height: auto;
  }
  .information_content h4{
    border-bottom: 1.5px solid black;
    margin-bottom: 30px;
    width: 35%;
    text-align: left;
    font-weight: 600;
  }
  .information_content th{
    font-size: 1.1rem;
    font-weight: 600;
    vertical-align: top;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    padding-right: 3rem;
    padding-top: 10px;
    line-height: 2.5;
  }
  .information_content td{
    font-size: 1rem;
    font-weight: 600;
    font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
    line-height: 2.5;
  }
  /*Bootstrap 樣式調整*/
  .carousel-indicators{
    justify-content: end!important;
    margin: 0 !important;
    width: 100% !important;
    height: auto !important;
  }
  .carousel-indicators button {
    border-radius: 50% !important;
    border: 2.2px solid rgb(251, 231, 78) !important;
    width: 15px !important;
    height: 15px !important;
    background-color: #ffffff !important;
}
.carousel-item img{
  width: 500px !important;
  height: auto !important;
}
@media only screen and (max-width:900px){ /*RWD : 900px*/
  .information_pic{  /*固定點播圖的size 寬度需和img一樣，否則指示器會跑位*/
    width:420px;
    height: auto;
    padding: 3rem 1rem;
  }
  .information_content h4{
    margin-bottom: 10px;
    width: 45%;

  }
  .carousel-item img{
    width:420px !important;
    height: auto !important;
  }
}

@media only screen and (max-width:767px){   /*   RWD: 767px */
/*商店資訊*/
.information{
  display: flex;
  flex-direction: column;
} 
.information_pic{  /*固定點播圖的size 寬度需和img一樣，否則指示器會跑位*/
  max-width:100%;
  height: auto;
  align-items: center;
}
.information_container{
  max-width:30%;
  height: auto;
  line-height: 2;

}
.information_content{
  display: flex;
  flex-direction: column;
  align-items: center;
  max-width: 100%;
  height: auto;
}
.information_content h4{
  border-bottom: 0px solid black;
  margin-bottom: 30px;
  width: 100%;
  text-align: center;
  font-weight: 600;
}
.information_content th{
  font-size: 3.2vw;
  font-weight: 700;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  padding: 0;
  padding-right: 6rem;
  line-height: 4;
}
.information_content td{
  text-align: left;
  font-size: 2.8vw;
  font-weight: 600;
  font-family: 'Franklin Gothic Medium', 'Arial Narrow', Arial, sans-serif;
  line-height: 2.8;
}
/*Bootstrap 樣式調整*/
.carousel-indicators{
  justify-content: center!important;
  margin: 0 !important;
  width: 100% !important;
  height: auto !important;
}
.carousel-indicators button {
  border-radius: 50% !important;
  border: 2.2px solid rgb(251, 231, 78) !important;
  width: 15px !important;
  height: 15px !important;
  background-color: #ffffff !important;
}
.carousel-item img{
  max-width:100%;
  height: auto;
}
/*商店資訊*/
}
</style>