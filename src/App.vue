<template>
  <div
    id="app"
    class="min-h-screen min-w-full justify-center flex bg-[#0c0f14] text-white"
  >
    <router-view v-slot="{ Component }">
      <transition name="fade" mode="out-in">
        <component :is="Component" />
      </transition>
    </router-view>
  </div>
</template>
