<template>
    <div class="h-screen bg-rose-50 ">
        <Hero />
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 1440 320"><path fill="#f43f5e " fill-opacity="1" d="M0,224L60,224C120,224,240,224,360,197.3C480,171,600,117,720,128C840,139,960,213,1080,250.7C1200,288,1320,288,1380,288L1440,288L1440,0L1380,0C1320,0,1200,0,1080,0C960,0,840,0,720,0C600,0,480,0,360,0C240,0,120,0,60,0L0,0Z"></path></svg>
        
    </div>
</template>

<script>

import Hero from '@/components/Hero.vue';

export default {
  name: "App",
  components: {
    Hero,
  },
};

</script>
