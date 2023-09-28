<template>
  <div class="box_all">
    <div class="col" v-for="(n, i) in travelList" :key="n">
      <div class="card">
        <img :src="n.img" class="card-img-top" alt="Travel Destination">
        <div class="card-body">
          <h3 class="card-title">{{ n.name }}</h3>
          <p class="card-text">ราคาโต๊ะ: {{ n.price }} บาท</p>
          <h6 class="card-subtitle">*** จำกัด 5 คนต่อ 1 โต๊ะ ***</h6>
          <button class="btn btn-primary" @click="list_local_control(n.name, n.quantity)">จองโต๊ะ</button>
        </div>
      </div>
    </div>
  </div>
</template>


<script setup>

import { ref } from 'vue';

const travelList=ref([
{name: 'ท่าช้าง คาเฟ่',  price:200, img:"https://scontent.fcnx3-1.fna.fbcdn.net/v/t1.15752-9/382327664_1388798415320739_3384383021365675584_n.png?_nc_cat=102&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeGw0ulmiyZOtO0PoY6xeo0ygDpatV1rd2WAOlq1XWt3ZXfgho0dM3wWkdraAw8cMLFj0RDvUcjeYDeIOkBY3FIO&_nc_ohc=uFc2_Re2q1wAX8geFPx&_nc_ht=scontent.fcnx3-1.fna&oh=03_AdQQ1cEAcMx7gTCR_IDzJniOkiaPqUZRmJuw6LtPYOHLng&oe=653D1F22", quantity: 0 ,
    text_box:'ใครที่เป็นสายชิลล์ สายปาร์ตี้ บอกเลยว่าถ้าไปเชียงใหม่ทั้งทีก็ต้องไปแวะเช็คอินร้านชื่อดังอย่าง “ร้านท่าช้าง” ✨ นั่นเองจ้า ซึ่งร้านนี้เรียกได้ว่าเป็นร้านใหญ่ขวัญใจวัยรุ่นชาวเชียงใหม่เลย มีนักท่องเที่ยวมากมายที่ต้องแวะเวียนกันไปเช็คอินสักครั้ง มีความน่าสนใจอะไร วันนี้บทความนี้จะพาเพื่อนๆ ไปเช็คอินท่าช้างกันแบบ Exclusive เลยจ้า  ถ้าพร้อมแล้วก็ตามมาเลย '
    }])


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