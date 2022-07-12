<template>
  <div>
    <p><slot name="counter1" /></p>
    <p><slot name="counter2" /></p>
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
