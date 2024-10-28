<!--  -->
<template>


    <section class="common-seciton">

        <h1 class="common-title">最新消息</h1>

        <div class="content-box">

            <div class="article-item">
                <div class="article-img-box">
                    <img class="article-img" src="@/assets/img/team-img-01.png">
                </div>

                <div class="article-info-box">
                    <h2 class="article-title">怡馨調心成長工作房-中區</h2>
                    <p class="article-description">身體與心理是一體的兩面，兩者有著互相影響、密不可分的關係，今年我們邀請芳療師和身體工作的經絡老師，來跟大家分享如何運用香氣、經絡按摩的方法來照顧好自己的身體與心理，才有更多力量面對生活的種種挑戰，歡迎大家一起來學期吧</p>
                </div>

            </div>

        </div>
    </section>

</template>

<script setup lang='ts'>

import { ref, reactive } from 'vue'

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

    }

    .content-box {
        margin-left: 10%;
    }
}
</style>
