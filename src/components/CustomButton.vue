<template>
  <button :type="type" :class="className" class="btn btn-yellow">
    {{ text }}
  </button>
</template>

<script>
  export default {
    name: "CustomButton",
    props: {
      text: {
        type: String,
        required: true,
      },
      className: {
        type: String,
      },
      type: {
        type: String,
      },
    },
  };
</script>