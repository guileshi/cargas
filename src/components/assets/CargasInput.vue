<template>
  <div class="input__field">
    <label :for="labelFor" class="input__label"> {{ labelTitle }} </label>
    <input
      :type="inputType"
      :name="inputName"
      :placeholder="inputPlaceholder"
    />
  </div>
</template>

<script>
export default {
  props: {
    labelFor: {
      type: String,
      required: true,
    },
    labelTitle: {
      type: String,
      required: true,
    },
    inputType: {
      type: String,
      required: true,
    },
    inputName: {
      type: String,
      required: true,
    },
    inputPlaceholder: {
      type: String,
      required: true,
    },
  },
};
</script>