<script setup>

</script>

<template>

<div class="menu_cover">
    <div class="menu_img">
        <img src="./assets/menu-cover.png" style="width:90%;height:30vw;">
    </div>
</div>

<div class="menu_header"><h4>Price Menu</h4></div>
<div class="menu">
    <div class="menu-section">
      <div class="menu-title"><span>Coffee</span></div>
      <div class="item"><span class="item-name">Classic Latte<br>經典拿鐵</span><span class="item-price">$180 ~</span></div>
      <div class="item"><span class="item-name">Cappuccino<br>卡布奇諾</span><span class="item-price">$180 ~</span></div>
      <div class="item"><span class="item-name">Iced Americano<br>冰美式咖啡</span><span class="item-price">$160 ~</span></div>
      <div class="item"><span class="item-name">Espresso<br>義式濃縮咖啡</span><span class="item-price">$150 ~</span></div>
    </div>
    <div class="menu-section">
      <div class="menu-title"><span>Cookies</span></div>
      <div class="item"><span class="item-name">American Chocolate Cookie<br>美式巧克力軟餅</span><span class="item-price">$60</span></div>
      <div class="item"><span class="item-name">Cheese Cookie<br>起司餅乾</span><span class="item-price">$60</span></div>
      <div class="item"><span class="item-name">Strawberry Cookies<br>草莓餅乾</span><span class="item-price">$60</span></div>
    </div>
    <div class="menu-section">
        <div class="menu-title"><span>Drinks</span></div>
        <div class="item"><span class="item-name">Bubble Milk Tea<br>珍珠奶茶</span><span class="item-price">$100</span></div>
        <div class="item"><span class="item-name">Mango Ice<br>芒果冰沙</span><span class="item-price">$80</span></div>
        <div class="item"><span class="item-name">Chocolate Ice<br>巧克力冰沙</span><span class="item-price">$80</span></div>
      </div>
      <div class="menu-section">
        <div class="menu-title"><span>Coffee</span></div>
        <div class="item"><span class="item-name">Chocolate Cake<br>巧克力蛋糕</span><span class="item-price">$80</span></div>
        <div class="item"><span class="item-name">Strawberry Cake<br>草莓蛋糕</span><span class="item-price">$80</span></div>
        <div class="item"><span class="item-name">Creamy Cake<br>奶油蛋糕</span><span class="item-price">$80</span></div>
      </div>
    </div>
<div class="extra_container">
    <div class="menu_extra">
      <div class="extra_column">
        <h3>奶類</h3>
        <p>低指牛奶 <span>+ $0</span></p>
        <p>燕麥奶 <span>+ $10</span></p>
        <p>奶粉<span>+ $0</span></p>
      </div>
      <div class="extra_column">
        <h3>口味</h3>
        <p>抹茶粉<span>+ $5</span></p>
        <p>巧克力粉 <span>+ $5</span></p>
        <p>起司粉<span>+ $5</span></p>
      </div>
      <div class="extra_column">
        <h3>飲料</h3>
        <p>特大杯 650ml <span>+ $15</span></p>
        <p>大杯 420ml <span>+ $10</span></p>
        <p>中杯 320ml <span>+ $0</span></p>
      </div>
    </div>
</div>
<div class="annotations">
    <p>* Additional ingredients may cause extra charge.</p>
    <p>* Prices are subject to change without notice.</p>
</div>

</template>

<style lang="scss">
.menu_body{
    display: flex;
    justify-content: center;
}
.menu_cover{
    padding: 8rem 0;
}
.menu_img{
    display: flex;
    justify-content: center;
    width: 100%;
    height: 20vh;
}
.menu_header{
    display: flex;
    justify-content: center;
    padding-top:250px;
    h4{
        font-size: 24px;
        font-weight: 600;
        border-bottom: 1.5px solid black;
        line-height: 2;
    }
}
.menu{
    display: grid;
    grid-template-columns: auto auto;
    gap: 3rem;
    font-family: 'Arial', sans-serif;
    padding:1rem 10rem;
}
  .menu-section {
    display: grid;
    padding: 0 2rem;
    gap: 10px;
}
.menu-title{
    font-size: 1.5em;
    text-align: left;
    padding:3rem 0;
    span{
        border: 2px solid rgb(99, 97, 97);
        padding: 3px;
        border-radius: 10px 10px 2px 2px;
        background-color: #fffbfb;
    }
}
.item{
    display: flex;
    justify-content: space-between;
    line-height: 2;
}
.item-name {
    font-weight: 600;
    font-family: sans-serif;
}
.item-price {
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 600;
    font-size: 14px;
    padding-top: 5px;
}
.extra_container{
    max-width: 100%;
    height: auto;
    padding:2rem 10rem;
}
.menu_extra{
    display: flex;
    justify-content: space-between;
    max-width: 100%;
    line-height: 3;
}
.extra_column h3 {
    margin-bottom: 20px;
}
  
.extra_column p{
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 700;
    margin: 10px 0;
}
.annotations{
    max-width: 600px;
    margin: 20px auto;
    font-size: 0.8em;
}

.annotations{
    margin: 0;
    padding:1rem 10rem;
    font-family: Arial, Helvetica, sans-serif;
    font-weight: 600;
}
@media only screen and (max-width:900px){ /*RWD : 900px*/
.menu_header{
    display: flex;
    justify-content: center;
    padding-top:1rem ;
}
.menu{
    display: grid;
    grid-template-columns: auto auto;
    gap: 3rem;
    font-family: 'Arial', sans-serif;
    padding:1rem 1rem;
}
.extra_container{
    max-width: 100%;
    height: auto;
    padding:2rem 4rem;
}
.annotations{
    padding: 0rem 4rem;
}
}

@media only screen and (max-width:767px){   /*   RWD: 767px */
  /*菜單品項*/
  .menu_cover{
    padding: 5rem 0;
  }
  .menu-section {
    display: grid;
    padding: 0;
    gap: 10px;
  }
  .extra_container{
    padding: 4rem 1rem;
    font-size: 2.5vw;
  }
  .annotations{
    padding-left:1rem ;
  }
  /*菜單品項*/
  }
</style>
