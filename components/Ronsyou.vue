<template>
<div>
    <v-card
    class="mx-auto"
    @click.stop="data.isDialog = true"
    >
        <v-img
        src="/ronsyou_search.png"
        class="img"
        max-height="400"
        />
        <v-divider></v-divider>
        <v-card
        flat>
            <v-card-text class="text-center">
                みんなの論証集
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
                            みんなの論証集
                        </v-card-title>
                        <v-card-text>
                            <p>司法試験論文式試験を解くためには、法的論点に対する解答（論証）を身につけることが必須です。本アプリではユーザーが自分オリジナルの論証集を作り、他のユーザーと共有することができます。</p>
                        </v-card-text>
                        <v-card-title>
                            使用技術
                        </v-card-title>
                        <v-card-text>
                            <span>react</span>
                            <span>/</span>
                            <span>mui</span>
                            <span>/</span>
                            <span>laravel</span>
                            <span>/</span>
                            <span>mysql</span>
                            <span>/</span>
                            <span>docker</span>
                            <span>/</span>
                            <span>aws ecs</span>
                        </v-card-text>
                        <v-card-title>
                            機能
                        </v-card-title>
                        <v-card-text>
                            <span>ログイン</span>
                            <span>/</span>
                            <span>投稿機能</span>
                            <span>/</span>
                            <span>いいね機能</span>
                            <span>/</span>
                            <span>ストック機能</span>
                            <span>/</span>
                            <span>検索機能</span>
                        </v-card-text>
                        <v-card-subtitle>
                            ソースコード
                        </v-card-subtitle>
                        <v-card-text>
                            <a
                            href="https://github.com/kota926/ronsyou-app"
                            target="_blank" rel="noopener noreferrer"
                            >https://github.com/kota926/ronsyou-app</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サイトURL
                        </v-card-subtitle>
                        <!-- <v-card-text>
                            <a
                            href='https://lawexam.link/login'
                            target="_blank" rel="noopener noreferrer"
                            >https://lawexam.link/login</a>
                        </v-card-text> -->
                        <v-card-text>
                            <p
                            href='https://lawexam.link/login'
                            target="_blank" rel="noopener noreferrer"
                            >https://lawexam.link/login（停止中）</p>
                        </v-card-text>
                        <v-card-subtitle>
                            サンプルアカウント
                        </v-card-subtitle>
                        <v-card-text>
                            <div>
                                <span class="mr-2">メール</span>
                                <span class="mr-2">:</span>
                                <span>sample1@sample.com</span>
                            </div>
                            <div>
                                <span class="mr-2">パスワード</span>
                                <span class="mr-2">:</span>
                                <span>sample_1</span>
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
                            src="/ronsyou_login.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/ronsyou_home.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/ronsyou_list.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/ronsyou_search.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/ronsyou_draw.png"
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
.carousel {
    object-fit: cover;
}
</style>