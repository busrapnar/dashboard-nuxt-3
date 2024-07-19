<template>
    <div
      class="flex flex-col gap-4 border w-1/4 rounded-lg shadow-sm px-2 py-2"
    >
      <div class="flex flex-col gap-0.5 items-center">
        <img src="" alt="" class="w-20 h-20 rounded-full border bg-black">
        <p class="font-semibold">PrimeTek</p>
        <span class="text-sm text-gray-600">@primatek</span>
      </div>
      <div class="flex items-center justify-around">
        <button >
          <Icon icon="ion:call-outline" class="w-5 h-5 text-gray-600"/>
        </button>
        <button>
          <Icon icon="icons8:video-call" class="w-5 h-5 text-gray-600"/>
        </button>
        <button>
          <Icon icon="ic:outline-login" class="w-5 h-5 text-gray-600"/>
        </button>
        <button>
          <Icon icon="solar:danger-circle-outline" class="w-5 h-5 text-gray-600"/>
        </button>
        <button>
          <Icon icon="heroicons-outline:dots-vertical" class="w-5 h-5 text-gray-600"/>
        </button>
      </div>
    </div>
</template>
<script setup>
import { Icon } from "@iconify/vue";
</script>