<template>
  <v-btn prepend-icon="$vuetify">
    {{ buttonText }}
  </v-btn>
</template>
  
<script>
  export default {
    props: {
      buttonText: {
        type: String,
        default: 'Click me'
      }
    }
  }
</script>
  