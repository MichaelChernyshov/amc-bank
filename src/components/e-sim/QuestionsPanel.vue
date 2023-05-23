<script>
export default {
    props: {
      titleF: String,
      textF: String,
      titleS: String,
      textS: String,
      titleT: String,
      textT: String,
    },
  }
</script>

<template>
    <div class="d-flex flex-column align-center">
    <div class="questions w-75 d-flex flex-column align-center">
        <h1 class="text-h4 pb-3">Popular questions</h1>
        <v-expansion-panels
        theme="dark"
        class="text-subtitle-1"
        >
            <v-expansion-panel
            :title=titleF
            :text=textF
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleS
            :text=textS
            bg-color="#154acf26"
            >
            </v-expansion-panel>
            <v-expansion-panel
            :title=titleT
            :text=textT
            bg-color="#154acf26"
            >
            </v-expansion-panel>
        </v-expansion-panels>
    </div>
</div>
</template>

<style lang="scss">
.v-expansion-panel-title {
  font-size: 1.2rem;
}
</style>