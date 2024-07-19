<template>
    <div class="flex gap-4 h-screen">
        <div class="rounded-lg py-4 pl-4">
            <Sidebar/>
        </div>
        <div class="p-4 h-screen overflow-y-scroll w-full">
            <slot/>
        </div>
    </div>
</template>
<script setup>
import Sidebar from '../components/Sidebar'
</script>