<template>
<div>
    <v-card
    class="mx-auto"
    @click.stop="data.isDialog = true"
    >
        <v-img
        src="/choice_quiz.png"
        class="img"
        max-height="400"
        />
        <v-divider></v-divider>
        <v-card
        flat>
            <v-card-text class="text-center">
                短答式問題集２
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
                            短答式対策問題集２
                        </v-card-title>
                        <v-card-text>
                            <p>司法試験の短答式試験の対策を行うアプリです。最後に解いた問題から再開する機能があります。</p>
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
                            <span>前回から再開</span>
                        </v-card-text>
                        <v-card-subtitle>
                            ソースコード
                        </v-card-subtitle>
                        <v-card-text>
                            <a
                            href="https://github.com/kota926/choice-app"
                            target="_blank" rel="noopener noreferrer"
                            >https://github.com/kota926/choice-app</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サイトURL
                        </v-card-subtitle>
                        <v-card-text>
                            <a
                            href='https://lawexam.link/login'
                            target="_blank" rel="noopener noreferrer"
                            >https://lawexam.link/login</a>
                        </v-card-text>
                        <v-card-subtitle>
                            サンプルアカウント
                        </v-card-subtitle>
                        <v-card-text>
                            <div>
                                <span class="mr-2">メール</span>
                                <span class="mr-2">:</span>
                                <span>sample@sample.com</span>
                            </div>
                            <div>
                                <span class="mr-2">パスワード</span>
                                <span class="mr-2">:</span>
                                <span>passpass</span>
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
                            src="/choice_login.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/choice_home.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/choice_quiz.png"
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