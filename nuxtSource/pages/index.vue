<template>
  <div>
    <section class="flex w-screen h-screen a4 page">
      <h1 v-t="'welcome'" class="m-auto text-4xl" />
    </section>
    <section class="flex w-screen h-screen a4 page">
      <h1 class="m-auto text-4xl">Section 2</h1>
    </section>
    <section class="flex w-screen h-screen a4 page">
      <h1 class="m-auto text-4xl">Section 3</h1>
    </section>
  </div>
</template>

<script>
export default {
  head: {
    title: 'Dynamic title',
  },
}
</script>

<style></style>
