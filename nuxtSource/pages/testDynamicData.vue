<template>
  <div>
    <section class="flex flex-col w-screen h-screen a4 page">
      <h1 class="m-auto text-4xl">{{welcomeTitle}}</h1>
      <h6 class="m-auto">welcome are testing different kinds of data here</h6>
    </section>
    <section class="flex flex-col w-screen h-screen a4 page" v-for="page in pages" :key="page.title">
      <h1 class="m-auto text-4xl">{{page.title}}</h1>
      <component :is="page.name" :class="page.pageCss"/>
    </section>
  </div>
</template>
<script>
import ImageComponent from '../components/imageComp.vue';
import CssComponent from '../components/cssComponent.vue';
import CanvasComponent from '../components/canvasComp.vue';

export default {
  components: {
    ImageComponent,
    CssComponent,
    CanvasComponent,
  },
  head: {
    title: 'Dynamic data test',
  },
  data() {
    return {
      welcomeTitle: "Welcome",
      pages: [
        {
          name: 'ImageComponent',
          title: "Image test",
          pageCss: ['margin-center']
        },
        {
          name: 'CssComponent',
          title: "CSS test",
          pageCss: ['margin-center']
        },
        {
          name: 'CanvasComponent',
          title: "Canvas test",
          pageCss: []
        }
      ]
    }
  },
}
</script>

<style>
.page{
  border: 2px solid black; /* remove this in production */  
}
/* .canvas-css {
  margin: 0 36%;
} */
.margin-center {
  margin: auto;
}
</style>
