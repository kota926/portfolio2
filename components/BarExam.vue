<template>
<div>
    <v-card
    class="mx-auto"
    @click.stop="data.isDialog = true"
    >
        <v-img
        src="/bar_app.png"
        class="img"
        max-height="400"
        />
        <v-divider></v-divider>
        <v-card
        flat>
            <v-card-text class="text-center">
                短答式試験対策アプリ
            </v-card-text>
        </v-card>
    </v-card>
    <v-dialog
    v-model="data.isDialog"
    >
        <v-card>
            <v-row
            class="mx-auto"
            >
                <v-col
                md="4"
                lg="5"
                >
                     <v-card
                    flat
                    >
                        <v-card-title>
                            短答式試験対策アプリ
                        </v-card-title>
                        <v-card-text>
                            <p>司法試験予備試験短答式の過去問を解くことができるアプリです。ユーザー登録することで、各科目の各単元の既解答数と最後に答えた問題を記録します。</p>
                        </v-card-text>
                        <v-card-title>
                            使用技術
                        </v-card-title>
                        <v-card-text>
                            <span>nuxt</span>
                            <span>/</span>
                            <span>vuetify</span>
                            <span>/</span>
                            <span>express</span>
                            <span>/</span>
                            <span>mysql</span>
                            <span>/</span>
                            <span>docker</span>
                            <span>/</span>
                            <span>aws ecs</span>
                        </v-card-text>
                        <v-card-subtitle>
                            ソースコード
                        </v-card-subtitle>
                        <v-card-text>
                            <a
                            href="https://github.com/kota926/bar-exam"
                            target="_blank" rel="noopener noreferrer"
                            >https://github.com/kota926/bar-exam</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サイトURL
                        </v-card-subtitle>
                        <v-card-text>
                            <p
                            
                            target="_blank" rel="noopener noreferrer"
                            >https://lawapp.link/auth（停止中）</p>
                        </v-card-text>
                        <v-card-subtitle>
                            サンプルアカウント
                        </v-card-subtitle>
                        <v-card-text>
                            <div>
                                <span class="mr-2">ユーザー名</span>
                                <span class="mr-2">:</span>
                                <span>test</span>
                            </div>
                            <div>
                                <span class="mr-2">パスワード</span>
                                <span class="mr-2">:</span>
                                <span>test2022</span>
                            </div>
                        </v-card-text>
                    </v-card>
                </v-col>
               <v-col
               md="8"
               lg="7"
               >
                   <v-card>
                        <v-carousel>
                            <v-carousel-item
                            src="/bar_exam_unit_list.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/bar_exam_answering.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/bar_exam_question_list.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/bar_exam_signin.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/bar_exam_user.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/bar_exam_aws_drowing.png"
                            class="carousel"
                            ></v-carousel-item>
                            <!-- <v-carousel-item
                            src="/bar_exam_er_drowing.png"
                            class="carousel"
                            ></v-carousel-item> -->
                            <!-- <v-carousel-item>
                                <img
                                src="/bar_exam_unit_list.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_answering.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_question_list.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_signin.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_user.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_aws_drowing.png"
                                class="carousel"
                                >
                            </v-carousel-item>
                            <v-carousel-item>
                                <img
                                src="/bar_exam_er_drowing.png"
                                class="carousel"
                                >
                            </v-carousel-item> -->
                        </v-carousel>
                    </v-card>
               </v-col>
            </v-row>
        </v-card>
    </v-dialog>
</div>
</template>

<script lang="ts">
import { defineComponent, reactive } from '@nuxtjs/composition-api'

export default defineComponent({
    setup () {
        const data = reactive({
            isDialog: false,
        })

        return {
            data
        }
    }
})
</script>

<style scoped>
.img {
    object-fit: cover;
}
.carousel {
    object-fit: cover;
}
</style>