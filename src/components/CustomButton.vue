<template>
  <a href="#" :class="className" class="btn about__btn">{{ text }}</a>
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
    },
  };
</script>