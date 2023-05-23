<script>
export default {
    props: {
      titleA: String,
      textA: String,
    },
  }
</script>

<template>
    <div class="questions d-flex flex-column align-center">
    <div class="w-75 d-flex flex-column align-center">
        <h1 class="text-h4 pb-3">Popular questions</h1>
        <v-expansion-panels
        theme="dark"
        >
            <v-expansion-panel
            :title=titleA
            :text=textA
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleA
            :text=textA
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleA
            :text=textA
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleA
            :text=textA
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleA
            :text=textA
            bg-color="#154acf26"
            >
            </v-expansion-panel>
        </v-expansion-panels>
    </div>
</div>
</template>

<style lang="scss">
</style>