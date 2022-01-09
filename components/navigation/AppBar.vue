<template>
    <v-app-bar
      :clipped-left="clipped"
      fixed flat app dense
      class="px-6"
    >
        <v-toolbar-title v-text="title" class="appTitle"/>
        <v-spacer />

        <ProfileBar />
    </v-app-bar>
</template>

<script lang="ts">
import { ref, defineComponent } from '@nuxtjs/composition-api'
import ProfileBar from '~/components/navigation/ProfileBar.vue'

export default defineComponent({
    name: 'AppBar',
    components: { ProfileBar },
    setup () {
        const title = ref('CHESS')
        const clipped = ref(false)
        const drawer = ref(false)
        const fixed = ref(false)
        const miniVariant = ref(false)
        const right = ref(false)

        return {
            title,
            clipped,
            drawer,
            fixed,
            miniVariant,
            right,
        }
    }
})
</script>

<style scoped>
.appTitle {
    font-family: Helvetica, sans-serif;
    font-size: 24px;
    font-weight: bold;
}
.appMenu {
    font-family: Helvetica, sans-serif;
    font-size: 16px;
    font-weight: bold;
    color: black;
}
</style>