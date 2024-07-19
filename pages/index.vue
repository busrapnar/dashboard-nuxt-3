<template>
  <div class="grid gap-8">
    <div class="flex flex-col gap-4">
      <header class="flex items-start justify-between gap-8">
        <div class="flex flex-col gap-2">
          <h1 class="text-lg text-gray-700 font-semibold">Overview</h1>
          <div class="flex gap-2 items-center">
            <h1 class="text-3xl font-bold">Good Morning, Robin</h1>
            <Icon icon="twemoji:waving-hand" class="w-7 h-7" />
          </div>
        </div>
        <div class="flex gap-2">
          <div
            class="flex justify-center border rounded items-center gap-2 px-4"
          >
            <Icon icon="ic:baseline-search" class="w-6 h-6" />
            <InputText placeholder="Search" />
          </div>
          <div class="border p-2 rounded">
            <Icon icon="ion:notifications-outline" class="w-6 h-6" />
          </div>
        </div>
      </header>
      <div class="flex justify-between">
        <div
          class="flex items-center gap-4 border rounded px-0.5 py-0.5 bg-gray-100 font-medium">
          <button class="bg-white px-2 py-1 text-center rounded font-medium">
            Monthly
          </button>
          <button class="px-2 py-1 text-center text-gray-500">Weekly</button>
          <button class="px-2 py-1 text-center text-gray-500">Daily</button>
        </div>
        <div class="flex items-center">
          <button class="bg-black text-white px-2 py-1.5 rounded flex gap-1">
            Download
            <Icon icon="carbon:download" class="w-6 h-6" />
          </button>
          <div class="flex-auto">
            <DatePicker showIcon class="border rounded-md px-4 py-1.5 mx-4" />
          </div>
        </div>
      </div>
      <div class="border rounded shadow-sm p-4">
        <Charts />
      </div>
      <div class="flex xl:flex-row justify-between gap-4 flex-col">
        <div class="xl:w-3/4 w-full border rounded-lg p-4">
          <h1>Transactions</h1>
          <Transactions />
        </div>
        <div class="xl:w-1/4 w-full border rounded-lg p-4">Wallet</div>
      </div>
    </div>
  </div>
</template>
<script setup>
import { Icon } from "@iconify/vue";
import { ref } from "vue";
import DatePicker from "primevue/datepicker";
</script>
