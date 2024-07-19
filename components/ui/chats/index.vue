<template>
    <div
      class="flex flex-col gap-4 border w-1/4 rounded-lg shadow-sm px-2 py-2 min-h-screen"
    >
      <div class="flex justify-between items-center">
        <span class="text-xl font-semibold">Chats</span>
        <button class="text-2xl font-medium">+</button>
      </div>
      <div class="flex items-center border rounded py-1">
        <Icon icon="ic:baseline-search" class="w-6 h-6" />
        <input placeholder="Search" class="" />
      </div>
      <div class="flex justify-between gap-1 bg-gray-300 px-0.5 py-0.5 rounded">
        <button class="bg-white w-1/2 text-center rounded font-medium " >Chat</button>
        <button class="w-1/2 text-center rounded bg-white">Call</button>
      </div>
      <div class="flex flex-col gap-4 ">
        <div class="flex gap-4 items-center relative hover:bg-slate-100 transition-all px-1 py-0.5 rounded-md">
            <div class="relative">
                <img
            class="w-10 h-10 rounded-full"
            src="https://images.pexels.com/photos/25677021/pexels-photo-25677021/free-photo-of-peyzaj-manzara-daglar-koy.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
            alt="logo"
          />
          <span class="w-2.5 h-2.5 rounded-full bg-green-500 absolute right-0.5 top-0"></span>
            </div>
          
          <div class="flex flex-col text-sm gap-1">
            <span class="font-bold">PrimeTek Team</span>
            <span class="text-xs">Hey There! </span>
          </div>
          <div class="flex flex-col gap-1 items-end">
            <span class="text-xs text-gray-500">11.25</span>
            <span class="w-4 h-4 rounded-full bg-black text-xs text-white text-center">8</span>
          </div>
        </div>
        <div class="flex gap-4 items-center hover:bg-slate-100 px-1 py-0.5 rounded-md transition-all">
          <img
            class="w-10 h-10 rounded-full"
            src="https://images.pexels.com/photos/25677021/pexels-photo-25677021/free-photo-of-peyzaj-manzara-daglar-koy.jpeg?auto=compress&cs=tinysrgb&w=1260&h=750&dpr=1"
            alt="logo"
          />
          <div class="flex flex-col text-sm gap-1">
            <span class="font-bold">PrimeTek Team</span>
            <span class="text-xs">Hey There! </span>
          </div>
          <div class="flex flex-col gap-1 items-end">
            <span class="text-xs text-gray-500">11.25</span>
            <span class="w-3 h-3 rounded-full border"></span>
          </div>
        </div>
      </div>
    </div>
</template>