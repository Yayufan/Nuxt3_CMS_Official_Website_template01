<!--  -->
<template>

    <Breadcrumbs firstRoute="認識器捐" secoundRoute="器官捐贈會刊"></Breadcrumbs>

    <section class="common-seciton">

        <h1 class="common-title">器官捐贈會刊</h1>

        <div class="content-box">

            <article class="article-item" v-for="(item, index) in bookArticleList.records " :key="index">

                <div class="article-info-box">
                    <h2 class="article-title">NO.
                        <span class="number">{{ item.title }}</span>
                        <br>
                        電子會刊
                    </h2>
                </div>

            </article>

        </div>


    </section>


</template>

<script setup lang='ts'>

import { ref, reactive } from 'vue'
import Breadcrumbs from '@/components/layout/Breadcrumbs.vue'


let bookArticleList = reactive({
    pages: 9,
    size: 9,
    records: [
        {
            title: '93',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '92',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '91',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '90',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '89',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '88',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '87',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '86',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '85',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '84',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '83',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '82',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '81',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '80',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '79',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '78',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '77',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '76',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '75',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
        {
            title: '74',
            description: '簽署器捐同意書有年齡限制嘛？',
            imgUrl: '/img/default-article-img.jpg',
        },
    ]
})




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
        margin-bottom: 3%;

        @media screen and (max-width:481px) {
            margin-left: 0;
        }
    }

    .content-box {
        margin-left: 10%;
        margin-right: 10%;
        display: flex;
        flex-wrap: wrap;
        justify-content: space-between;

        @media screen and (max-width:481px) {
            margin-left: 0;
        }

        .article-item {
            display: flex;
            flex-direction: column;
            justify-content: center;
            align-items: center;
            margin-bottom: 5%;
            border-radius: 50%;
            border: 3px solid $main-content-color;
            box-shadow: 4px 4px 4px rgba(0, 0, 0, 0.3);
            width: 200px;
            height: 200px;
            transition: 0.5s;

            //當滑鼠碰到這篇文章時,改變字體顏色+圖片放大
            &:hover {
                cursor: pointer;

                background: $sub-color ;

                .article-info-box {
                    color: #fff;
                }

            }

            @media screen and (max-width:480px) {
                width: 75%;
                margin: 0 auto;
            }


            .article-info-box {
                color: $sub-color;

                .article-title {
                    font-size: 1.5rem;

                    .number {
                        font-size: 3rem;
                    }

                }

            }

        }

    }
}
</style>