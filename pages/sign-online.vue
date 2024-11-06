<template>
    <Breadcrumbs firstRoute="簽署器捐" secoundRoute="線上簽署"></Breadcrumbs>
    <div class="common-section">
        <h1 class="common-title">線上簽署</h1>

        <div class="content-box">
            <p class="title">器官捐贈同意書</p>
            <div class="statement">
                <p>本人瞭解醫療有其極限，而愛心可以延續，經閱讀，知悉後列說明後，願意簽署<span class="donation-form"><b><u>【器官捐贈同意書】</u></b></span>，</p>
                <p>並將此意願註記於健保卡，於生命之盡頭，捐贈可用器官，讓其他需要的病人能因此而獲得重生機會。</p>
                <p>如須撤銷器捐同意，請下載<span class="cancel-form"><b><u>【撤銷器捐同意書】</u></b></span>填寫後由寄正本到本會。</p>
            </div>
        </div>
        <div class="form-section">
            <p class="notice">(以下欄位有<span>*</span>標示者為必填)</p>
            <el-form ref="ruleFormRef" class="form" :rules="formRules" label-position="left">
                <el-form-item label="簽署人：" label-width="270" prop="name" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="國民身分證統一編號：" prop="ID" label-width="270" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="出生日期：" label-width="270" prop="birthday" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="連絡電話：" label-width="270" prop="contactNumber" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="手機號碼：" label-width="270" prop="phoneNumber" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="E-Mail：" label-width="250" prop="email" class="unnecessary email">
                    <el-input class="email-input"></el-input>
                </el-form-item>
                <el-form-item label="聯絡地址：" label-width="270" prop="address" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="法定代理人姓名：" label-width="270" prop="legalRepresentativeName" class="form-item1">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="法定代理人國民身分證統一編號：" class="legal-representative-ID" prop="legalRepresentativeID">
                    <el-input></el-input>
                </el-form-item>
                <el-form-item label="本人獲得器官捐贈同意卡：" class="unnecessary form-item1">
                    <el-radio-group>
                        <el-radio label="希望"></el-radio>
                        <el-radio label="不希望"></el-radio>
                    </el-radio-group>
                </el-form-item>
                <div class="text-area">
                    <el-form-item class="reason unnecessary" label="簽署的原因：" label-width="auto">
                        <el-input></el-input>
                    </el-form-item>
                    <el-form-item class="word-to-family unnecessary" label="給家人的話：" label-width="auto">
                        <el-input></el-input>
                    </el-form-item>
                </div>
                <el-form-item class="donate-organs unnecessary" label="願意捐贈器官/組織項目(可複選)">
                    <el-checkbox-group>
                        <div class="checkbox-div">
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                        </div>
                        <div class="checkbox-div">
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                        </div>
                        <div class="checkbox-div">
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                            <el-checkbox label="全部捐贈"></el-checkbox>
                        </div>
                    </el-checkbox-group>
                </el-form-item>
            </el-form>
        </div>
    </div>
</template>
<script lang="ts" setup>
import Breadcrumbs from '@/components/layout/Breadcrumbs.vue'
import type { FormInstance, FormRules } from 'element-plus'


const ruleFormRef = ref<FormInstance>()
const formRules = {
    name: [
        { required: true, message: '請輸入簽署人', trigger: 'blur' }
    ],
    ID: [
        { required: true, message: '請輸入國民身分證統一編號', trigger: 'blur' }
    ],
    birthday: [
        { required: true, message: '請輸入出生日期', trigger: 'blur' }
    ],
    contactNumber: [
        { required: true, message: '請輸入連絡電話', trigger: 'blur' }
    ],
    phoneNumber: [
        { required: true, message: '請輸入手機號碼', trigger: 'blur' }
    ],
    address: [
        { required: true, message: '請輸入聯絡地址', trigger: 'blur' }
    ],
    legalRepresentativeName: [
        { required: true, message: '請輸入法定代理人姓名', trigger: 'blur' }
    ],
    legalRepresentativeID: [
        { required: true, message: '請輸入法定代理人國民身分證統一編號', trigger: 'blur' }
    ]

}
</script>
<style lang="scss" scoped>
.common-section {
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

        @media screen and (max-width:481px) {
            margin-left: 0;
        }

        .title {
            background-color: $main-color;
            color: white;
            // width: 10vw;
            display: inline-block;
            text-align: center;
            padding: 5px 15px;
            letter-spacing: 0.1rem;
            border-radius: 35px;
        }

        .statement {
            color: $main-content-color;
            max-width: 80%;
            margin: 1% 0 0 10%;
            font-size: 1rem;
            @media screen and (max-width:850px) {
                max-width: 100%;
                margin: 1% 0 0 0;
                font-size: 0.9rem;
                
            }
            p {
                @media screen and (max-width:850px) {
                    display: inline;
                    
                }
            }
        }

        .donation-form {
            color: $main-color;
            padding: 0 5px;
            font-size: 1.3rem;
            @media screen and (max-width:850px) {
                font-size: 1rem;
            }
        }

        .cancel-form {
            color: #F49E19;
            padding: 0 5px;
            font-size: 1.3rem;
            @media screen and (max-width:850px) {
                font-size: 1rem;
            }
        }
    }

    .notice {
        color: $main-content-color;
        margin: 3% 0 3% 5%;

        span {
            color: red;
        }
    }

    .form-section {
        background-color: #F2F2F1;
        padding: 1% 10%;
        // display: flex;
        // justify-content: center;

        .form {
            .form-item1,
            .legal-representative-ID {
                :deep(.el-form-item__label) {
                    font-size: 1.3rem;
                    color: black;
                    // min-width: 27%;

                    @media screen and (max-width:850px) {
                        font-size: 0.9rem;
                        width: 40% !important;

                    }
                }

                .el-radio {
                    margin-right: 0;
                }

                :deep(.el-radio__label) {
                    font-size: 1.3rem;
                    color: black;

                    @media screen and (max-width:850px) {
                        font-size: 0.9rem;
                        width: 60% !important;

                    }
                }

            }

            .email {
                :deep(.el-form-item__label) {
                    margin-right: 0.3rem;
                    // min-width: 25.5%;


                    @media screen and (max-width:850px) {
                        margin-right: 0;
                        font-size: 0.9rem;
                        width: 39% !important;

                    }
                }

                .el-input {
                    width: 100%;
                    margin: 0 auto;
                    @media screen and (max-width:850px) {
                        width: 100%;
                    }
                }
            }

            .text-area {
                display: flex;

                @media screen and (max-width:850px) {
                    display: block;
                }

                .reason,
                .word-to-family {
                    display: block;
                    width: 50%;

                    @media screen and (max-width:850px) {
                        width: 100%;

                    }

                    .el-input {
                        min-height: 15vw;
                        width: 100%;

                        @media screen and (max-width:850px) {
                            min-height: 20vw;

                        }

                        :deep(.el-input__wrapper) {
                            border-radius: 25px;
                        }
                    }
                }
            }

            .unnecessary {
                padding-left: 0.9rem;

                :deep(.el-form-item__label) {
                    font-size: 1.3rem;
                    color: black;

                    @media screen and (max-width:850px) {
                        font-size: 0.9rem;
                        width: 65%;

                    }
                }
            }

            .legal-representative-ID {
                :deep(.el-form-item__label) {
                    @media screen and (max-width:850px) {
                        font-size: 0.9rem;
                        width: 45% !important;
                    }
                }
            }

            .el-input {
                width: 100%;


                margin: 0 auto;

                @media screen and (max-width:850px) {
                    width: 100%;
                }
            }

            .donate-organs {
                display: block;
                max-width: 100%;

                @media screen and (max-width:850px) {
                    max-width: 100%;
                }

                .el-checkbox-group {
                    width: 100%;

                    .checkbox-div {
                        display: flex;

                        @media screen and (max-width:850px) {
                            justify-content: space-between;

                        }
                    }
                }

                .el-checkbox {
                    margin-top: 1rem;
                    margin-right: 8vw;
                    max-width: 100%;

                    @media screen and (max-width:850px) {
                        max-width: 100%;
                        margin-right: 0;
                    }
                }

                :deep(.el-checkbox__label) {
                    font-size: 1.3rem;
                    color: $main-content-color;

                    @media screen and (max-width:850px) {
                        font-size: 0.9rem;
                        width: 60% !important;
                        margin-right: 0rem;

                    }
                }
            }

        }
    }
}
</style>