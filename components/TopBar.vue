<template>
    <v-app-bar
    flat
    fixed
    color="white"
    >
        <v-sheet
        width="600"
        class="ml-auto mx-auto"
        >
            <v-tabs
            grow
            v-model="activeTab"
            >
                <v-tab
                v-scroll-to="'#top'"
                >TOP</v-tab>
                <v-tab
                v-scroll-to="{ el: '#work', offset: -80}"
                >WORK</v-tab>
                <v-tab
                v-scroll-to="{ el: '#skill', offset: -30}"
                >SKILL</v-tab>
            </v-tabs>
        </v-sheet>  
    </v-app-bar>
</template>

<script lang="ts">
import { defineComponent, ref, reactive, computed, useContext, onMounted, watch } from '@nuxtjs/composition-api'

export default defineComponent({
    setup (props,  context) {
        const works = ref(null)
        const activeTab = ref(0)
        const scrollY = ref(0)
        const workLocation = ref(0)
        const skillLocation = ref(0)

        window.addEventListener('scroll', () => {
            const workElement = document.getElementById('work')
            const skillElement = document.getElementById('skill')
            scrollY.value = window.scrollY
            workLocation.value = workElement.getBoundingClientRect().top
            skillLocation.value = skillElement.getBoundingClientRect().top
        })
        watch(scrollY, () => {
            if(skillLocation.value <= 30) {
                activeTab.value = 2
            } else if(workLocation.value <= 80) {
                activeTab.value = 1
            } else {
                activeTab.value = 0
            }
        })
        return {
            activeTab,
        }
    }
})
</script>

<style scoped>

</style>