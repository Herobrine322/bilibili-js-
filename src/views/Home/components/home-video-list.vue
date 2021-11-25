<template>
    <div class="list">
        <AppVideoItem v-for="item in list" :key="item.id" :video="item" />
    </div>
</template>
<script setup>
import { ref } from 'vue'
import axios from 'axios'
import AppVideoItem from '@/components/app-video-item.vue'

const list = ref([])
axios({
    method: 'get',
    url: '/videosList'
}).then(res => {
    console.log('视频列表的数据', res.data.result)
    list.value = res.data.result
})
</script>
<style>
.list {
    display: flex;
    flex-wrap: wrap;
    padding: 0 1vw;
}
</style>