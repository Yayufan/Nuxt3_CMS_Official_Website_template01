<!--  -->
<template>

    <Breadcrumbs firstRoute="簽署器捐" secoundRoute="簽卡停看聽"></Breadcrumbs>

    <section class="common-seciton">

        <h1 class="common-title">簽卡停看聽</h1>

        <div class="schematic-diagram-box">
            <div class="schematic-item green-block ">健保IC卡註記</div>
            <div class="schematic-item yellow-block">器捐卡遺失</div>
            <div class="schematic-item red-block ">法定代理人</div>
            <div class="schematic-item blue-block">簽卡管道</div>
            <div class="schematic-item orange-block">B肝帶原</div>
        </div>

        <div class="content-box">

            <article class="paragraph">

            </article>


        </div>


    </section>


</template>

<script setup lang='ts'>

import { ref, reactive } from 'vue'
import Breadcrumbs from '@/components/layout/Breadcrumbs.vue'

</script>

<style scoped lang="scss">
.common-seciton {
    width: $common-section-width;
    margin: $common-section-margin;
    font-family: $common-section-font-family;

    .common-title {
        color: $main-color;
        font-weight: $common-title-font-weight;
        font-size: $common-title-font-size;
        letter-spacing: $common-title-letter-spacing;
        margin-left: 10%;
        margin-bottom: 2%;

        @media screen and (max-width:481px) {
            margin-left: 0;
        }
    }

    .schematic-diagram-box {
        margin-left: 5%;
        display: flex;
        justify-content: flex-start;
        align-items: center;
        font-size: 1.3rem;
        font-weight: 600;


        .schematic-item {
            padding: 1rem 0;
            color: #fff;
            flex: 1;
            text-align: center;



            &:first-child {
                border-radius: 18px 0 0 18px;
            }

            &:last-child {
                border-radius: 0 18px 18px 0;
            }

        }

    }

    .content-box {
        margin-left: 10%;

        @media screen and (max-width:481px) {
            margin-left: 0;
        }

        .additional-information {
            margin-left: 1.7rem;
            margin-bottom: 5rem;
            font-size: 1rem;
            max-width: 900px;
            line-height: 1.5;
        }

        .paragraph {
            margin: 3% 0;
        }

        .sub-title {
            font-size: 1.2rem;
        }

        .download-file-box {
            display: flex;
            flex-direction: column;
            margin-left: 2.5rem;

            .download-link {
                margin: 0.5rem;
                /** 這邊是為了將a標籤從flex block 狀態,改為inline block 狀態  */
                align-self: flex-start;
            }

        }
    }
}


//不同顏色
.green-block {
    background: #94AA8F;
}

.yellow-block {
    background: #EEC46B;
}

.red-block {
    background: #C75A73;
}

.blue-block {
    background: #196B9C;
}

.orange-block {
    background: #F49E19;
}
</style>