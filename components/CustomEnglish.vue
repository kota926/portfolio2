<template>
<div>
    <v-card
    class="mx-auto"
    @click.stop="data.isDialog = true"
    >
        <v-img
        src="/custom.png"
        height="200"
        class="img"
        />
        <v-divider></v-divider>
        <v-card
        flat>
            <v-card-text class="text-center">
                カスタム英文帳
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
                            カスタム英文帳
                        </v-card-title>
                        <v-card-text>
                            <p>英単語を英文の中で覚えることを目的に作られた、ユーザーが単語帳を自作する英単語学習アプリです。</p>
                        </v-card-text>
                        <v-card-title>
                            使用技術
                        </v-card-title>
                        <v-card-text>
                            <span>nuxt</span>
                            <span>/</span>
                            <span>vuetify</span>
                            <span>/</span>
                            <span>aws amplify</span>
                            <span>/</span>
                        </v-card-text>
                        <v-card-subtitle>
                            ソースコード
                        </v-card-subtitle>
                        <v-card-text>
                            <a href="https://github.com/kota926/word-list">https://github.com/kota926/word-list</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サイトURL
                        </v-card-subtitle>
                        <v-card-text>
                            <a href="https://master.d1pazmes2f7ewt.amplifyapp.com/">https://master.d1pazmes2f7ewt.amplifyapp.com/</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サンプルアカウント
                        </v-card-subtitle>
                        <v-card-text>
                            <div>
                                <span class="mr-2">ユーザー名</span>
                                <span class="mr-2">:</span>
                                <span>sample</span>
                            </div>
                            <div>
                                <span class="mr-2">パスワード</span>
                                <span class="mr-2">:</span>
                                <span>sample2022</span>
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
                            src="/custom_login.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/custom_top_page.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/custom_list.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/custom_test.png"
                            class="carousel"
                            ></v-carousel-item>
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
</style>