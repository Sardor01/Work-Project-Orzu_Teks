<template>
  <a :href="link" :class="className" class="btn btn-yellow">
    {{ text }}
  </a>
</template>

<script>
  export default {
    name: "CustomLink",
    props: {
      text: {
        type: String,
        required: true,
      },
      className: {
        type: String,
      },
      link: {
        type: String,
      },
    },
  };
</script>