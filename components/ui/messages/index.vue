<template>
    <div class="flex flex-col gap-4 border w-2/4 rounded-lg shadow-sm">
      <div class="flex flex-col">
        <div class="border-b">
          <div class="flex gap-3 items-center px-2 py-2">
            <div class="w-auto">
              <img src="" alt="" class="border rounded-full w-12 h-12" />
            </div>
            <div class="flex flex-col gap-1 text-xs w-2/3">
              <span class="font-medium text-sm">PrimeTek</span>
              <span class="text-gray-400">Cody Fisher, Esther Howard</span>
            </div>
            <div class="flex items-center gap-2 w-1/3">
              <button>
                <Icon icon="ion:call-outline" class="w-6 h-6 text-gray-500" />
              </button>
              <button>
                <Icon icon="ic:outline-search" class="w-6 h-6 text-gray-500" />
              </button>
              <button>
                <Icon
                  icon="flowbite:dots-horizontal-outline"
                  class="w-6 h-6 text-gray-500"
                />
              </button>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>
<script setup>
import { Icon } from "@iconify/vue";
</script>