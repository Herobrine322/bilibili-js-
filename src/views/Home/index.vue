<template>
<!-- 头部组件 -->
<AppHeader/>
<!-- 频道组件 -->
<HomeChannel/>
<!-- 轮播组件 -->
<HomeSwipe />
<!-- 视频列表 -->
<HomeVideoList />

</template>
<script setup>
// script setup 只需要导入组件，无需注册
import AppHeader from '@/components/app-header.vue'
import HomeChannel from './components/home-channel.vue'
import HomeSwipe from './components/home-swipe.vue'
import HomeVideoList from './components/home-video-list.vue'
</script>
