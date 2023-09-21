<script setup>
import { ref } from 'vue';

const hotenInput = ref(null)


  function saveinfo(){
    console.log(hotenInput.value)
  }
</script>

<template>
  <div class="container mx-auto">
    <p class="text-3xl mt-5">Quản lý học sinh</p>
    <div class="flex justify-between m-10">
      <div class="ms-16">
        <label>Học sinh</label>
        <br>
        <input class="border border-black bg-gray-200 p-3 w-[300px]" v-model="hotenInput" />
      </div>
      <div>
        <label>Lớp</label>
        <br>
        <input class="border border-black bg-gray-200 p-3 w-[300px]" ref="lopInput"/>
      </div>
      <div class="self-end me-16">
        <button class="bg-blue-500 hover:bg-blue-700 text-white font-bold p-3 rounded" @click="saveinfo">Lưu</button>
      </div>
    </div>
    <p class="text-xl mb-2">Danh sách học sinh</p>
    <table class="w-full">
      <tr>
        <th class="border border-black w-[20%]">ID{{ }}</th>
        <th class="border border-black w-[40%]">Họ và tên</th>
        <th class="border border-black w-[40%]">Lớp</th>
      </tr>
    </table>
  </div>
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
