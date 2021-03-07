<template>
  <div
    class="d-flex flex-column mx-auto install-container h-100"
    style="padding-top: 120px; max-width: 800px"
  >
    <h1 class="header-text mx-4">
      Just a couple more steps to your very own PasteBucket
    </h1>
    <p class="description-text mx-4">
      You will need a machine that can run docker containers to host the
      pastebucket server on the network. Pastebucket will only work when this
      machine is turned on and connected to same network as your devices. For
      example a Raspberry Pi would be perfect for the task.
    </p>
    <div class="d-flex h-100">
      <div class="row w-100 h-100">
        <div class="col-md-6">
          <InstallCard title="Set up the server" :number="1">Hello</InstallCard>
        </div>
        <div class="col-md-6">
          <InstallCard title="Download the client" :number="2"
            >Hello</InstallCard
          >
        </div>
      </div>
    </div>
  </div>
</template>

<script lang="ts">
export default {
  transition: {
    name: 'fade',
  },
}
</script>

<style lang="scss" scoped>
.header-text {
  text-align: center;
  font-family: 'Lato', sans-serif;
  font-weight: 700;
  font-size: 40px;
}

.description-text {
  text-align: center;

  opacity: 0.3;
}

.install-container {
  min-height: 100vh;
}
</style>
