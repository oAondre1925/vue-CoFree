<script setup>

</script>

<template>
<div class="feature">
    <div class="feature_img">
        <img src="./assets/feature.png">
    </div>
    <div class="feature_head">
        <h4>Feature</h4>
        <p>「醇萃」咖啡館，一個位於都市繁華中的寧靜所在，每一杯咖啡都承載著對手藝的尊重與對時光的頌歌。
            這裡不僅是品味咖啡的場所，更是心靈對話的角落。<br>
            步入其中，濃郁咖啡香與溫暖氛圍迎面撲來，讓人在熙攘中找到安寧的庇護。
            無論您是尋求一段獨處的閒暇，或期待與摯友的溫馨相聚，「醇萃」總有一席之地，為您提供一個舒心的環境。
            在這裡，每一個細節都細緻入微，每一次來訪，都是一場關於咖啡的美好旅程。
        </p>
    </div>
</div>

       
<div class="feature_body">
    <div class="feature_center">
        <div class="feature_container">
                <div class="feature_item">
                    <img src="./assets/feature_cup.png" style="max-width: 75%; height: auto;">
                    <h4>品質</h4>
                    <p>我們堅持每一杯咖啡的卓越品質，精選頂級咖啡豆，手工烘焙至完美風味。</p>
                </div>
                <div class="feature_item">
                    <img src="./assets/feature_cup02.png" style="max-width: 75%; height: auto;">
                    <h4>再生</h4>
                    <p>為地球盡一份心，我們使用可回收材料，實踐環保再生的承諾。</p>
                </div>
                <div class="feature_item">
                    <img src="./assets/feature_cup03.png" style="max-width: 75%; height: auto;">
                    <h4>聆聽</h4>
                    <p>在這裡，每位顧客的意見都是我們進步的動力，我們聆聽您的每一個聲音。</p>
                </div>
                <div class="feature_item">
                    <img src="./assets/feature_cup04.png" style="max-width: 75%; height: auto;">
                    <h4>風格</h4>
                    <p>不只是咖啡，更是生活的態度。我們的獨特風格，讓您的每一刻都時尚非凡。</p>
                </div>
                <div class="feature_item">
                    <img src="./assets/feature_cup05.png" style="max-width: 75%; height: auto;">
                    <h4>技術</h4>
                    <p>專業的咖啡師，運用最先進的技術，為您沏出一杯杯質感生活的咖啡。</p>
                </div>
                <div class="feature_item">
                    <img src="./assets/feature_cup06.png" style="max-width: 75%; height: auto;"> 
                    <h4>多元</h4>
                    <p>我們擁抱多元文化，提供各式各樣的咖啡選擇，滿足您的每一種口味需求。</p>
                </div>
        </div>
    </div>
</div>

</template>

<style land="scss">
.feature{
    display: flex;
    flex-direction: column;
    max-width: 100%;
    height: auto;
    padding: 10rem 0;
    align-items: center;
    justify-content: space-around;
  }
  .feature_img{
    display: flex;
    justify-content: center;
    width: 100%;
    overflow: hidden;
  }
  .feature img{
    overflow: hidden;
    max-width: 85%;
    height: auto;
    transform:scale(1,1);
    transition: all 1.5s ease-out;
    &:hover{
        transform:scale(1.05,1.05);
    }
  }
  .feature_head{
    display: flex;
    padding: 1rem 10rem;
    max-width: 100%;
    height: auto;
    h4{
        padding-right:2rem ;
        font-size: 1.5rem;
        font-weight: 500;
    }
    p{
        margin: 0;
        font-family: sans-serif;
        font-size: calc(30 - 1vw);
        font-weight: 600;
        text-align: left;
        line-height: 2;
    }
  }

/*Feature Body*/
  .feature_body{
    display: flex;
    justify-content: center;
    min-height: 10vh;
    margin: 0; 
  }
  .feature_center{
    width: 1180px;
    border-top: solid 1.8px rgb(66, 65, 65);
  }
  .feature_container{
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 2rem;
    margin: 2rem;
  }
  .feature_item{
    padding: 10px;
    display: grid;
    grid-template-columns: repeat(4,1fr);
    grid-template-rows: auto; 
    img{
        display: flex;
        justify-content: center;
        align-items: center;
    }
    h4{
        text-align: left;
        margin-left: 25px;
        grid-column: 2/-1;
        font-size: 18px;
        font-family: 'Times New Roman', Times, serif;
    }
    p{
        padding-left: 10px;
        text-align: left;
        grid-column: 1/-1;
        line-height: 2;
        margin-top: 40px;
        font-family: sans-serif;
        font-weight: 600;
        vertical-align: top;
    }
  }
  @media only screen and (max-width:900px){   /*   RWD: 767px */

    .feature_head{
      padding: 1rem;
    }
    .feature_container{
      display: grid;
      grid-template-columns: repeat(2, 1fr);
      gap: 10px;
      margin: 4rem;
    }
  }

  @media only screen and (max-width:767px){ 

    /*商店特色(head)*/
  .feature{
    padding: 2rem 0;
  }
  .feature_head{
    display: flex;
    flex-direction: column;
    max-width: 100%;
    height: auto;
    padding: 1rem;
    h4 {
        font-family: 'Times New Roman', Times, serif;
        padding-bottom:1rem ;
        text-align: center;
    }
    p {
        margin: 0;
        font-family: sans-serif;
        font-size: calc(30 - 1vw);
        font-weight: 600;
        text-align: center;
        line-height: 1.5;
    }
  }
  .feature img:hover{
    transform:scale(1.05,1.05);
  }
/*商店特色(head)*/

/*商店特色詳細資訊*/
  .feature_container{
    display: grid;
    grid-template-columns: repeat(1, 1fr); 
    gap: 3rem; 
    margin: 2rem;
  }
  .feature_item img{
    grid-column: 1/2;
    margin: auto;
  }
  .feature_item h4{
    grid-column: 1/2;
    font-family: sans-serif;
    font-weight: 600;
    padding-top: 1rem;
    margin: auto;
    
  }
  .feature_item p{
    padding-left:1rem;
    margin: 0;
    grid-column: 2/5;
    grid-row: 1/3;
  }
/*商店特色詳細資訊*/
  }
</style>
