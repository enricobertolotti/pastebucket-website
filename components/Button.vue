<template>
  <div
    class="d-flex align-items-center rounded-button clickable"
    :class="filled ? 'button-filled' : 'button-outline'"
    @click="$emit('clicked')"
  >
    <p class="m-0">{{ buttontext }}</p>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component, Prop } from 'vue-property-decorator'

@Component({})
export default class Button extends Vue {
  @Prop({ default: 'Button' }) buttontext!: string
  @Prop({ default: false }) filled!: boolean
}
</script>

<style lang="scss" scoped></style>
