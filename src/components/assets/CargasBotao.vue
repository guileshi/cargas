<template>
  <button class="button" :type="buttonType" :class="buttonClass">
    {{ buttonTitle }}
  </button>
</template>

<script>
export default {
  props: {
    buttonTitle: {
      type: String,
      required: true,
    },
    buttonClass: {
      type: String,
      required: false,
    },
    buttonType: {
      type: String,
      required: true,
    },
  },
};
</script>