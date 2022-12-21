<template>
  <div class="w-full h-full flex flex-col justify-center items-center gap-4">
    <div>
      <div class="w-full max-w-2xl p-4 rounded bg-red-400 text-white">
        <div class="border-2 rounded flex flex-col md:flex-row md:items-center md:gap-8 p-4">
          <img src="/assets/santa.svg" alt="" class="max-w-[12em]" />
          <div>
            <h1 class="font-serif text-4xl">Happy Holidays!</h1>
            <div class="mt-4 bg-white text-black p-2 rounded">TO: {{ form.to }}</div>
            <div class="mt-2 bg-white text-black p-2 rounded">FROM: {{ form.from }}</div>
          </div>
        </div>
      </div>
    </div>

    <div class="w-full max-w-2xl p-4 rounded bg-red-400 text-black flex flex-col gap-2 max-w-sm">
      <div class="flex justify-between gap-4">
        <label class="text-white" for="to">To:</label>
        <input type="text" id="to" v-model="form.to" />
      </div>
      <div class="flex gap-4 justify-between">
        <label class="text-white" for="from">From:</label>
        <input type="text" id="from" v-model="form.from" />
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from 'vue'
const form = ref({
  to: '',
  from: '',
})
</script>
