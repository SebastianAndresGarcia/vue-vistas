<template>
  <v-container class="grey lighten-2" flex fill-height >
    <v-row md="12" justify="center" align="center">
    <editor 
    :other_options="tinyOptions"
      :init="{
        height: 700,
        width: '80%',
        plugins: 'lists link image table code help wordcount'
      }"
    />
  </v-row>
  </v-container>
</template>

<script>
import Editor from '@tinymce/tinymce-vue'

export default {
  name: 'EditorTiny',
  components: {
    'editor': Editor
  },
  tinyOptions: {
                    width: '5000px'
            }
}
</script>