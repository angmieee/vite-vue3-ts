<template>
    <h1> 测试 vueUse 的鼠标坐标 </h1>
    <h3>Mouse: {{ x }} x {{ y }}</h3>
</template>
    
<script lang="ts" setup>
import { defineComponent } from 'vue';
import { useMouse } from '@vueuse/core'
import request from '@/utils/axios';
const requestRes = async () => {
    let result = await request({
        url: '/api/xxx',
        method: 'get'
    });
}

const { x, y } = useMouse()
</script>
    