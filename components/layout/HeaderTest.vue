<template>
    <header class="PC-menu-box">
        <div class="logo-and-search-section">
            <div class="logo-box">
                <img ref="" class="logo" src="@/assets/img/logo.png" alt="logo"></img>
            </div>
            <div class="input-section">
                <el-input class="input" :suffix-icon="Search"></el-input>
            </div>
            <div class="contact-section">
                <nuxt-link class="contact" :to="'/'">聯絡我們</nuxt-link>
            </div>
        </div>
    </header>
</template>
<script lang="ts" setup>
import { Search } from '@element-plus/icons-vue'
</script>
<style lang="scss" scoped>
.logo-and-search-section {
    background-color: #FFFFFF;
    display: flex;
    padding-top: 1.5vw;

    .logo-box {
        flex-grow: 4;
        margin-left: 40vw;

        .logo {
            width: 20vw;
        }
    }

    .input-section {
        flex-grow: 1;
        display: flex;
        align-self: self-end;
        padding-bottom: 0.8vw;
        :deep(.el-input__wrapper) {
            background-color: $main-color;
            height: 1.5rem;
            width: 10rem;
            border-radius: 30px;
        }

        :deep(.el-input__suffix) {
            background-color: #FFFFFF;
            color: $main-color;
            padding-right: 1rem;
            height: 1rem;
            width: 0.8rem;
            border-radius: 10px;
        }
    }

    .contact-section {
        flex-grow: 1;
        // padding-bottom:3.8rem;
        padding-left: 2rem;
        display: flex;
        align-items: self-end;
        padding-bottom: 0.8vw;


        .contact {
            color: $main-color;
            font-size: 1rem;
        }
    }
}

</style>    