<template>
  <div class="box_all">
  <div class="col" v-for="(n,i) in travelList" :key="n">
    <div class="card" style="width: 25rem;" >
      <img :src="n.img" class="card-img-top">
      <div class="card-body">
        <h3 class="card-title">{{ n.name }}</h3>
        <p>ราคาโต๊ะ : {{n.price}}</p>
        <h6>***จำกัด 5 คนต่อ 1 โต๊ะ***</h6>

        <a class="btn btn-primary" @click="list_local_control(i.name, i.quantity)"> จองโต๊ะ </a>
      </div>
    </div>
  </div>
</div>

</template>

<script setup>

import { ref } from 'vue';

const travelList=ref([
{name:'Bang Kwang',  price:130,  img:"https://scontent.fcnx3-1.fna.fbcdn.net/v/t1.15752-9/382335057_816299076947913_2905298185714344693_n.png?_nc_cat=108&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeHuOZ1rKc2JUbwhSDeQr6zz1VDb1JB_OGHVUNvUkH84YQxpjLtjsyrtV0WPO-jCGLE3-BGAhNRD2c9k49pB9RgW&_nc_ohc=zt5qLCW8JsMAX-ZLU6c&_nc_oc=AQmkjR0WHpPGRtxP3MM1l_hA7w2DN9PW348B6h48PruX9GURYvr5LCHzU95goY6jrSQ&_nc_ht=scontent.fcnx3-1.fna&oh=03_AdTMKlZ3OcqX_x8GrhzjIGGhFOeknRzyXYRLZ_K69z_R2Q&oe=653D2CEF", quantity: 0 ,
    text_box:'ร้านนี้ไม่ได้เป็นเพียงแค่ร้านเหล้าปกติธรรมดา แต่ยังมีความพิเศษที่ทางร้านจัดให้กับลูกค้าในทุก ๆ วัน ไอ้ที่เคยมาที่นี่ต่างพูดเป็นเสียงเดียวกันว่า นี้นักร้องดังนักร้องเด็ด เพลงเพราะ อาหารอร่อย และเป็นร้านที่บรรยากาศดีเหมาะกับการนั่งชิวหรือนั่งดื่มสังสรรค์ในยามค่ำคืนเป็นอย่างมาก'
    },])


</script>
<style scoped>
.card {
  width: 18rem;
  margin: 20px;
  border: 1px solid #ddd;
  border-radius: 10px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.card-img-top {
  height: 200px;
  object-fit: cover;
  border-top-left-radius: 10px;
  border-top-right-radius: 10px;
}

.card-body {
  padding: 20px;
}

.card-title {
  font-size: 1.5rem;
  margin-bottom: 10px;
}

.card-text {
  font-size: 1.2rem;
}

.card-subtitle {
  font-size: 1rem;
  color: #888;
  margin-top: 10px;
}

.btn-primary {
  background-color: #007BFF;
  border: none;
  border-radius: 5px;
  color: #fff;
}

.btn-primary:hover {
  background-color: #0056b3;
}

.box_all {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  align-items: center;
  margin: 30px auto;
}
</style>
