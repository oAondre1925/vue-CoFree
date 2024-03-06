<script setup>

</script>

<template>
<div class="active_body">
    <div class="active">
        <div class="active_container">
            <div class="active_item">
                <img src="./assets/wallbook.png" > 
                <h3>其他活動</h3>
                <h4>Other activity</h4>
                <p>當您踏入這個獨特的空間，將會發現一個完美融合咖啡與知識的世界。這裡，我們精選了各式各樣的書籍，囊括文學、藝術、歷史、哲學、旅遊以及咖啡文化等豐富主題，為您打造一個理想的閱讀環境。在這個舒適的角落裡，您可以在柔軟的座椅上沉浸在書籍的海洋中，同時享受著咖啡的芬芳氣息。
                    無論您是尋求片刻的寧靜，還是渴望新知識的探索者，這裡的藏書角都將成為您的心靈棲息地。透過咖啡的溫暖和書籍的智慧，您將能夠找到心靈的慰藉和創意的靈感。在這裡，每一杯咖啡都伴隨著知識的啟發，每一本書都帶來獨特的體驗。                  
                    歡迎您來到這個充滿靈感與品味的閱讀天地，開啟一段屬於自己的美好旅程。讓咖啡的香氣和書頁的輕聲相伴，沉浸在這美妙的閱讀與品味之旅中。</p>
            </div>
        </div>
    </div>
</div>
</template>

<style lang="scss">
.active_body{
    display: flex;
    justify-content: center;
    min-height: 10vh; 
    margin: 0; 
  }
.active{
  width: 100%;
  h4{
    grid-row: 1; 
    color: rgb(126, 125, 125);
  }
}
.active_container{
  display: grid;
  grid-template-columns: repeat(1,1fr); 
  border: 1px solid rgb(222, 221, 221);
  background-color:#faf7f7;
  padding: 3rem 5rem;
}
.active_item{
  display: grid;
  grid-template-columns: repeat(3,1fr);
  grid-template-rows:auto auto 10px;
  gap: 10px;
  border-radius: 6px;
  img{
    grid-row: 1 / -1;
    width: 380px;
    height:320px; 
  }
h3{
      grid-row: 1; 
      font-family: 'Courier New', Courier, monospace;
}
    p{
        grid-column: 2/-1;
        line-height: 1.2;
        font-family: 'Courier New', Courier, monospace;
        font-weight: 600;
        font-size: 1rem;
        padding:1rem;
    }
}
@media only screen and (max-width:900px){ /*RWD : 900px*/
.active{
    width: 100%;
}
.active_container{
    display: grid;
    grid-template-columns: repeat(1,1fr); 
    border: 1px solid rgb(222, 221, 221);
    background-color:#faf7f7;
    padding: 1rem;
}
.active_item{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    grid-template-rows:auto auto 10px;
    gap: 10px;
    border-radius: 6px;
    img{
      grid-row: 1 / -1;
      width: 310px; 
      height:310px ;
      }
  }
}
@media only screen and (max-width:767px){   /*   RWD: 767px */
  .active{
    width: 100%;
    h4{
      grid-column: 2/-1;
      grid-row: 2/3; 
      color: rgb(126, 125, 125);
    }
  }
  .active_container{
    display: grid;
    grid-template-columns: repeat(1,1fr); 
    border: 1px solid rgb(222, 221, 221);
    background-color:#faf7f7;
    padding: 2rem;
  }
  .active_item{
    display: grid;
    grid-template-columns: repeat(3,1fr);
    grid-template-rows:auto auto;
    gap: 10px;
    border-radius: 6px;
    img{
          grid-column: 1 / -1;
          grid-row:1/2 ;
          width: 100%; 
          height:auto ; 
          padding: 0;
      }
      h3{
          grid-column: 1/2;
          grid-row: 2/3; 
          font-family: 'Courier New', Courier, monospace;
          text-align: left;
      }
      p{
          grid-column: 1/-1;
          grid-row: 3/-1;
          line-height: 2;
          font-family: 'Courier New', Courier, monospace;
          font-weight: 600;
          font-size: 1rem;
          padding: 0;
      }
  }
  /*商店活動*/
}
</style>
