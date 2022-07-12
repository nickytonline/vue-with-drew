<template>
  <div>
    <p>{{ counter }}</p>
    <p><slot /></p>
  </div>
</template>
<script>
export default {
  props: {
    counter: {
      type: Number,
      required: true,
    },
  },
}
</script>
