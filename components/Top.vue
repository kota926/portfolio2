<template>
    <v-sheet
    id="top"
    height="76vh"
    class="sheet d-flex align-center justify-center">
        <div class="text-center">
            <div class="text-h4 text-sm-h2 mb-4">Shimmura Kota</div>
            <div class="text-h5 text-sm-h4">I'm an engineer</div>
        </div>
    </v-sheet>
</template>

<script lang="ts">
import { defineComponent } from '@nuxtjs/composition-api'

export default defineComponent({
    setup () {
        

        return {}
    }
})
</script>

<style scoped>
.sheet {
    background-color: #f0f0f0f0;
    margin-top: 50px;
}
.name {
    color: black;
}
.main {
    font-size: 60px;
}
.sub {
    font-size: 40px
}
</style>