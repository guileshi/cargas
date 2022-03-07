<template>
  <a :href="linkPage" class="button" :class="buttonClass">
    {{ linkTitle }}
  </a>
</template>

<script>
export default {
  props: {
    linkTitle: {
      type: String,
      required: true,
    },
    buttonClass: {
      type: String,
      required: false,
    },
    linkPage: {
      type: String,
      required: true,
    },
  },
};
</script>