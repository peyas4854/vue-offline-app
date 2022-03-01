<template>
  <div class="flex w-screen h-screen text-gray-700">
    <div class="flex flex-col flex-shrink-0 w-64 border-r border-green-300 bg-green-100">
      <h1>sadsad</h1>
    </div>
    <div class="flex flex-col flex-grow">
      <h3> sdfsdfsd</h3>
    </div>
  </div>
</template>

<script>
import { Editor, EditorContent } from '@tiptap/vue-3'
import StarterKit from '@tiptap/starter-kit'

export default {
  name: 'App',
  data() {
    return {
      editor: null,
    }
  },
  components: {
    EditorContent,
  },
  mounted() {
    this.editor = new Editor({
      content: '<p>I’m running Tiptap with Vue.js. 🎉</p>',
      extensions: [
        StarterKit,
      ],
    })
  },

  beforeUnmount() {
    this.editor.destroy()
  },
}
</script>
