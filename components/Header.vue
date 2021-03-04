<template>
  <div class="d-flex w-100 justify-content-center py-4">
    <div
      class="d-flex w-100 justify-content-between align-items-center"
      style="max-width: 900px"
    >
      <div class="clickable" @click="$router.push('/')">
        <h4 id="logo-text">Pastebucket</h4>
      </div>
      <div class="d-flex align-items-center">
        <a
          href="https://github.com/enricobertolotti/pastebucket "
          target="_blank"
          class="link mr-3"
          >Github</a
        >
        <Button buttontext="Install" @clicked="$router.push('/install')" />
      </div>
    </div>
  </div>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped></style>
