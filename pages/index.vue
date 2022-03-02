<template>
    <div>
        <top-bar />
        <top />
        <work />
        <skill />
        <bottom-footer />
    </div>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'
import TopBar from '../components/TopBar.vue'
import Top from '../components/Top.vue'
import Work from '../components/Work.vue'
import BottomFooter from '../components/BottomFooter.vue'
import Skill from '../components/Skill.vue'

export default defineComponent({
  components: { TopBar, Top, Work, BottomFooter, Skill },
    setup () {
        
        return {}
    }
})
</script>

<style scoped>

</style>