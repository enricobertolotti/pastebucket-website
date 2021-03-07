<template>
  <div class="d-flex flex-column align-items-md-start h-100 mx-1">
    <div class="d-flex align-items-center">
      <div class="d-flex align-items-center justify-content-center number mr-3">
        <h5 class="m-0">{{ number }}</h5>
      </div>
      <h2 class="m-0">{{ title }}</h2>
    </div>
    <div class="card d-flex w-100 h-100 mt-3">
      <slot></slot>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'
import { Component, Prop } from 'vue-property-decorator'

@Component({})
export default class InstallCard extends Vue {
  @Prop({ required: true }) title!: string
  @Prop({ required: true }) number!: number
}
</script>

<style lang="scss" scoped>
.number {
  width: 35px;
  height: 35px;
  border-radius: 27px;
  background-color: white;
  color: black;
  h5 {
    font-weight: 800;
  }
}

.card {
  padding: 25px;
  background-color: #070707;
  border-radius: 15px;
}
</style>
