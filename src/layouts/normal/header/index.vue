<template>
  <AppCard class="flex items-center px-12" border-b="1px solid light_border dark:dark_border">
    <MenuCollapse />

    <AppTab class="w-0 flex-1 px-12" />

    <span class="mx-6 opacity-20">|</span>

    <div class="flex flex-shrink-0 items-center px-12 text-18">
      <BeginnerGuide />

      <ToggleTheme />

      <Fullscreen />

      <i
        class="i-fe:github mr-16 cursor-pointer"
        @click="handleLinkClick('https://github.com/wuchuuuuu')"
      />
      <i
        class="i-me:gitee mr-16 cursor-pointer"
        @click="handleLinkClick('https://gitee.com/wuchu990723')"
      />

      <ThemeSetting class="mr-16" />

      <UserAvatar />
    </div>
  </AppCard>
</template>

<script setup>
import { ToggleTheme } from '@/components'
import { AppTab, BeginnerGuide, Fullscreen, MenuCollapse, UserAvatar } from '@/layouts/components'

function handleLinkClick(link) {
  window.open(link)
}
</script>
