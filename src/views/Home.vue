<template>
  <div class="home p-20">
    <h1 class="text-2xl md:text-4xl font-bold mb-5">HOME PAGE</h1>
    <HelloWorld msg="Welcome to my webpage. I'm Calvin, a newbie programmer from Malaysia."/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld
  }
}
</script>
