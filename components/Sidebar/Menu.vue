<template >
    <div>
        <header class="items-center flex gap-2 p-4 hover:scale-[101%] transition cursor-pointer">
            <Logo />
            <p class="font-semibold text-2xl">Prime</p>
        </header>
        <div class="px-4 py-4 grow">
            <div class="grid gap-4">
                <a :href="item.path" v-for="(item, index) in items" :key="index" class="flex items-center gap-3 px-4 py-2 transition rounded cursor-pointer hover:bg-slate-900 hover:text-white active:bg-slate-900 active:text-white">
                    <Icon :icon="item.icon" class="h-5 w-5 shrink-0"  />
                    <span>{{ item.title }}</span>
                </a>
            </div>
        </div>
    </div>
</template>
<script setup>
import { Icon } from '@iconify/vue';
const items = ref([
    {
        title: 'Overview',
        path:'/',
        icon: 'ic:outline-home'
    },
    {
        title: 'Chat',
        path:'/chat',
        icon:'grommet-icons:chat'
    },
    {
        title: 'Inbox',
        path:'/inbox',
        icon:'ic:outline-account-circle'
    },
    {
        title: 'Cards',
        path:'/cards',
        icon: 'ic:outline-dashboard'
    },
    {
        title: 'Settings',
        path:'/settings',
        icon:'ant-design:setting-outlined'
    },
])
</script>