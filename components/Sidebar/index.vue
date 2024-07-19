<template>
    <div class="relative h-full rounded-lg shadow-lg bg-gray-100">
        <div class="flex flex-col xl:hidden z-50 gap-8 h-full w-full p-4">
            <Logo />
            <div>
                <a :href="item.path" v-for="(item, index) in items" :key="index"
                    class="flex items-center gap-3 px-4 py-2 transition rounded cursor-pointer hover:bg-slate-900 hover:text-white active:bg-slate-900 active:text-white">
                    <Icon :icon="item.icon" class="h-6 w-6 shrink-0" />

                </a>
            </div>
            
        </div>
        <div class="hidden xl:flex w-[250px] flex-col justify-between h-full">
            <SidebarMenu />
            <div class="flex flex-col gap-3 items-start px-4">
                <a href=""
                    class="flex items-center gap-3 w-full px-4 py-2 transition rounded cursor-pointer hover:bg-slate-900 hover:text-white active:bg-slate-900 active:text-white">
                    <Icon icon="ion:flag-outline" class="h-5 w-5 shrink-0" />
                    <button>Support</button>
                </a>
                <a href=""
                    class="flex items-center gap-3 w-full px-4 py-2 transition rounded cursor-pointer hover:bg-slate-900 hover:text-white active:bg-slate-900 active:text-white">
                    <Icon icon="ant-design:setting-outlined" class="h-5 w-5 shrink-0" />
                    <button>Settings</button>
                </a>
                <div class="flex gap-2 items-center mt-4 py-4">
                    <img src="https://images.pexels.com/photos/25677021/pexels-photo-25677021/free-photo-of-peyzaj-manzara-daglar-koy.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
                        alt="" class="border rounded-full w-12 h-12">
                    <div class="flex flex-col gap-1 ">
                        <span class="font-bold text-sm">Robin Jones</span>
                        <span class="text-black font-bold text-opacity-40 text-sm">@robinjones</span>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>
<script setup>
import { Icon } from '@iconify/vue';
const items = ref([
    {
        title: 'Overview',
        path: '/',
        icon: 'ic:outline-home'
    },
    {
        title: 'Chat',
        path: '/chat',
        icon: 'grommet-icons:chat'
    },
    {
        title: 'Inbox',
        path: '/inbox',
        icon: 'ic:outline-account-circle'
    },
    {
        title: 'Cards',
        path: '/cards',
        icon: 'ic:outline-dashboard'
    },
    {
        title: 'Settings',
        path: '/settings',
        icon: 'ant-design:setting-outlined'
    },
])
</script>