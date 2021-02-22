<template lang="pug">
.editor-content
  .title.is-1 Editor
  .container
    .field
      label.label title
      .control
        input.input

    .field
      label.label Content
      .control
        textarea.textarea.textarea-post
</template>

<style lang="sass" scoped>
.editor-content
  padding: 1rem

.textarea-post
  font-family:Consolas,Monaco,Lucida Console,Liberation Mono,DejaVu Sans Mono,Bitstream Vera Sans Mono,Courier New, monospace
</style>
