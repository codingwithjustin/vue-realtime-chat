<template>
  <img class="avatar" :src="src" />
</template>

<script>
export default {
  props: { src: { type: String, default: '' } }
}
</script>
