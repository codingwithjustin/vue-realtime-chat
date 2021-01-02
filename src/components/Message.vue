<template>
  <div class="message">
    <span v-if="!right">{{ name }}</span>
    <div class="flex" :class="right ? 'flex-row-reverse' : ''">
      <Avatar class="mt-1" :src="photoUrl" />
      <div class="text w-3/4" :class="right ? 'bg-green-800' : 'bg-gray-700'">
        <slot />
      </div>
    </div>
  </div>
</template>

<script>
import Avatar from './Avatar.vue'
export default {
  components: { Avatar },
  props: {
    name: { type: String, default: '' },
    photoUrl: { type: String, default: '' },
    right: { type: Boolean, default: false }
  }
}
</script>
