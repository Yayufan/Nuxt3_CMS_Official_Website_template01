<!--  -->
<template>

    <section class="common-seciton">

        <h1 class="common-title">加入會員</h1>

        <div class="content-box">

            <article class="paragraph">
                <h2 class="sub-title">會員類別</h2>
                <div class="individual-member-box">
                    <div class="common-label">個人會員</div>
                    <p>凡贊同本會宗旨，年滿二十歲，填具入會申請書</p>
                </div>
                <div class="group-member-box"></div>


                <div class="number-mask">1</div>

            </article>

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
        // background-color: aqua;
        width: 100%;
        color: $main-content-color;

        /**這邊是處理通用段落、sub-title 和 內容 */
        .paragraph {
            position: relative;
            min-height: 100px;
            border: 5px solid #E5E8E0;
            border-radius: 80px 40px 40px 40px;
            background-color: #fff;
            padding: 1% 4%;
            margin-bottom: 3%;


            .sub-title {
                color: #56575E;
                font-size: 1.3rem;
            }


            .number-mask {
                font-size: 2rem;
                background-color: #C5CEB6;
                /* 背景顏色 */
                color: white;
                /* 文字顏色 */
                border-radius: 50%;
                /* 圓形 */
                width: 2.5rem;
                /* 圓形寬度 */
                height: 2.5rem;
                /* 圓形高度 */
                display: inline-block;
                /* 使其為行內塊元素 */
                text-align: center;
                /* 文字置中 */
                line-height: 2.5rem;
                /* 行高等於圓形高度以置中 */
                position: absolute;
                /* 絕對定位 */
                left: 0;
                /* 相對於 li 的位置 */
                top: 7%;
                /* 垂直置中 */
                transform: translateY(-50%);
                /* 調整位置至垂直中心 */
            }

        }

    }

}
</style>
