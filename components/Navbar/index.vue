<template>
    <div class="flex justify-between items-center py-4">
        <div class="flex gap-4">
            <select class="w-60 border rounded-md">
                <option value="Alicia Koch"></option>
            </select>
            <div>
            <ul class="flex gap-4">
                <li v-for="item in items" :key="item.title">
                    <NuxtLink :to="item.path">
                        <span>{{ item.title }}</span>
                    </NuxtLink>
                </li>
            </ul>
        </div>
        </div>
        <div>
            User
        </div>
    </div>
</template>
<script setup>
const items = ref([
{
        title: 'Overview',
        path:'/',
        icon: 'ic:outline-dashboard'
    },
    {
        title: 'Customers',
        path:'/customers',
        icon:'grommet-icons:transaction'
    },
    {
        title: 'Products',
        path:'/products',
        icon:'ic:outline-account-circle'
    },
    {
        title: 'Settings',
        path:'/settings',
        icon:'ant-design:setting-outlined'
    },
])
</script>