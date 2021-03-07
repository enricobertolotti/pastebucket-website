<template>
  <div class="d-flex flex-column align-items-md-start">
    <div class="d-flex">
      <div class="number">
        <p class="m-0">{{ number }}</p>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Prop } from 'vue-property-decorator'

export default class InstallCard extends Vue {
  @Prop({ required: true }) title!: string
  @Prop({ required: true }) number!: string
}
</script>

<style lang="scss" scoped>
.number {
  width: 54px;
  height: 54px;
  border-radius: 27px;
}
</style>
