<template>
<div>
    <v-card
    class="mx-auto"
    @click.stop="data.isDialog = true"
    >
        <v-img
        src="/sem_img.png"
        class="img"
        height="200"
        />
        <v-card
        flat>
            <v-card-text class="text-center">
                ゼミホームページ
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
                            ゼミホームページ
                        </v-card-title>
                        <v-card-text>
                            <p>私が所属する大学のゼミほホームページです。htmlを知らない人も編集できるように、ヘッドレスCMSを利用してコンテンツの管理を外部からできるようにしました。</p>
                        </v-card-text>
                        <v-card-title>
                            使用技術
                        </v-card-title>
                        <v-card-text>
                            <span>nuxt</span>
                            <span>/</span>
                            <span>vuetify</span>
                            <span>/</span>
                            <span>prismic.io</span>
                        </v-card-text>
                        <v-card-subtitle>
                            サイトURL
                        </v-card-subtitle>
                        <v-card-text>
                            <a
                            href="https://www.waseda.jp/sem-kanazawa/"
                            target="_blank" rel="noopener noreferrer"
                            >https://www.waseda.jp/sem-kanazawa/</a>
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
                            src="/sem_top_page.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/sem_about.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/sem_archive.png"
                            class="carousel"
                            ></v-carousel-item>
                            <v-carousel-item
                            src="/sem_prismic.png"
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