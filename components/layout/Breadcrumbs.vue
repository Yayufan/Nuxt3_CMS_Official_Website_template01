<template>
    <div class="breadcrumbs">
        <el-breadcrumb class="breadcrumb" :separator-icon="ArrowRight">
            <el-breadcrumb-item :to="{ path: '/' }">首頁</el-breadcrumb-item>
            <el-breadcrumb-item>{{ firstRoute }}</el-breadcrumb-item>
            <el-breadcrumb-item>{{ secound }}</el-breadcrumb-item>
        </el-breadcrumb>
    </div>
</template>
<script lang="ts" setup>
    import { ArrowRight } from '@element-plus/icons-vue'

    const firstRoute = '加入我們';
    const secound = '協會年表';
</script>
<style lang="scss" scoped>
.breadcrumbs {
    padding: 20px 0;
    width: 100vw;
    background-color: #EAEAE9;
    display: flex;
    justify-content: center;

    .breadcrumb {
        width: 55%;
        display: flex;
        line-height: 100%;
        font-size: 1rem;
        font-weight: normal;
        letter-spacing: 0.1rem;
        color: $main-content-color;
        justify-content: flex-start;
    }
}
</style>