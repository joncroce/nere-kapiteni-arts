<script setup lang="ts">
  const showPortfolioMenu = ref(false)
</script>

<template>
  <header class="h-24 pb-4 flex justify-between items-stretch">
    <div class="flex flex-col justify-center items-start">
      <img src="/logo.jpg" class="w-16 h-16" />
      <div class="font-sans font-bold text-gray-500 text-xs">Making Art Move</div>
    </div>
    <nav class="pt-2 flex flex-nowrap justify-end items-baseline gap-16">
      <div class="relative inline-block" @mouseenter="showPortfolioMenu = true" @mouseleave="showPortfolioMenu = false">
        <div class="nav-item hover:text-dark-500" :class="showPortfolioMenu ? 'text-dark-500 cursor-default' : ''">portfolio <div class="text-gray-7 text-sm" :class="showPortfolioMenu ? 'i-entypo-chevron-down' : 'i-entypo-chevron-right'" /></div>
        <div v-if="showPortfolioMenu" class="absolute z-50 bg-white min-w-64 flex-col justify-start items-start gap-16 text-left">
          <div class="nav-item"><div i-entypo-air class="nav-icon" />motion graphics</div>
          <div class="nav-item"><div i-entypo-blackboard class="nav-icon" />logos & design boards</div>
          <div class="nav-item"><div i-entypo-brush class="nav-icon" />illustrations</div>
          <div class="nav-item"><div i-entypo-video class="nav-icon" />animated shorts</div>
        </div>
      </div>
      <div class="nav-item">about <div i-entypo-emoji-happy class="text-gray-7 text-sm"/></div>
      <div class="nav-item">contact<div i-entypo-email class="text-gray-7 text-sm"/></div>
    </nav>
  </header>
</template>
