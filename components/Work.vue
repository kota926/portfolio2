<template>
    <div>
        <div
        class="card text-center text-h4 text-md-h2"
        id="work"
        >Works
        </div>
        <v-container class="contain">
            <v-row>
                <v-col
                xs="6"
                sm="6"
                >
                    <ronsyou />
                </v-col>
                <v-col
                xs="6"
                sm="6"
                >
                    <bar-exam />
                </v-col>
                <v-col
                xs="6"
                sm="6"
                >
                    <custom-english />
                </v-col>
                <v-col
                xs="6"
                sm="6"
                >
                    <sem-site />
                </v-col>
            </v-row>
        </v-container>
    </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import BarExam from './BarExam.vue'
import CustomEnglish from './CustomEnglish.vue'
import Ronsyou from './Ronsyou.vue'
import SemSite from './SemSite.vue'

export default defineComponent({
  components: { BarExam, CustomEnglish, SemSite, Ronsyou },
    setup () {
        

        return {}
    }
})
</script>

<style scoped>
.contain {
    max-width: 500px;
    margin-bottom: 50px; 
    /* margin: 10px auto 70px; */
}
.card {
    margin: 74px 0 70px;
}
</style>