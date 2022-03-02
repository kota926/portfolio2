<template>
    <div
    class="back"
    >
        <div
        class="text-center card text-h4 text-md-h2"
        id="skill"
        >Skills
        </div>
        <v-container class="contain">
            <v-card>
                <v-card-text class="text-center">
                    フロントエンド
                </v-card-text>
                <v-card-text class="text-center">
                    <v-chip
                    outlined
                    color="success"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        vue.js
                    </v-chip>
                    <v-chip
                    outlined
                    color="green accent-4"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        nuxt
                    </v-chip>
                    <v-chip
                    outlined
                    color="primary"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        vuetify
                    </v-chip>
                </v-card-text>
            </v-card>
            <v-card class="my-10">
                <v-card-text class="text-center">
                    バックエンド
                </v-card-text>
                <v-card-text class="text-center">
                    <v-chip
                    outlined
                    color="success"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        node.js
                    </v-chip>
                    <v-chip
                    outlined
                    color="red accent-3"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        GraphQL
                    </v-chip>
                    <v-chip
                    outlined
                    color="orange"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        Mysql
                    </v-chip>
                </v-card-text>
            </v-card>
            <v-card class="my-10">
                <v-card-text class="text-center">
                    DevOps
                </v-card-text>
                <v-card-text class="text-center">
                    <v-chip
                    outlined
                    color="orange"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        AWS ECS
                    </v-chip>
                    <v-chip
                    outlined
                    color="orange"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        AWS amplify
                    </v-chip>
                    <v-chip
                    outlined
                    color="primary"
                    class="text-subtitle-1 mx-3 my-1"
                    >
                        Docker
                    </v-chip>
                </v-card-text>
            </v-card>
        </v-container>
    </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import BarExam from './BarExam.vue'
import CustomEnglish from './CustomEnglish.vue'
import SemSite from './SemSite.vue'

export default defineComponent({
  components: { BarExam, CustomEnglish, SemSite },
    setup () {
        

        return {}
    }
})
</script>

<style scoped>
.contain {
    max-width: 600px;
}
.card {
    padding: 74px 0 70px;
}
.back {
    background-color: #f0f0f0f0;
    
}
</style>