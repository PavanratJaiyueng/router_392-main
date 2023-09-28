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
{name:'Overnight',  price:190, img:"https://scontent.fcnx3-1.fna.fbcdn.net/v/t1.15752-9/384476175_1065885924416120_612714583375669465_n.png?_nc_cat=101&ccb=1-7&_nc_sid=ae9488&_nc_eui2=AeF97KyXbwco6H1QCt5qH3-8LV4oRHtJ5hgtXihEe0nmGGig2eHS_csE7BZgqxc7PPavMIUz69x3oXw30DaxDpd9&_nc_ohc=ZeZT3allpcQAX-jTZvQ&_nc_oc=AQkHST0muGUlIZR-HgKkP3c7dIqnOfVrt6v8KH57gtqXMC0v8Z1K3TIgxVmhSoo-wsM&_nc_ht=scontent.fcnx3-1.fna&oh=03_AdTyIlCCJ-bYYod3N_l9HTWXF8uwsmpNHIJtgK3qvjbjkA&oe=653D06D9", quantity: 0 ,
    text_box:'มาดื่มด่ำบรรยากาศแสนชิว พร้อมเครื่องดื่มและอาหารราคาสบายกระเป๋า มีดนตรีสดและดีเจทุกวัน '
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
