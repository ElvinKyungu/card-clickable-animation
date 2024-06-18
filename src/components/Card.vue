<script setup lang="ts">
import gsap from 'gsap';
import { ref } from 'vue';
const props = defineProps({
  image: String,
  title: String,
  subtitle: String,
  paragraphe: String
})
const showParagraph = ref(false);

const handleCardClick = (event: Event) => {
  const cardElement = event.currentTarget as HTMLElement;
  showParagraph.value = !showParagraph.value;

};
</script>
<template>
  <article
    @click="handleCardClick"
    class="
      px-5 py-2 bg-gray-800 cursor-pointer transition-colors text-white 
      rounded-xl mx-24
    "
  >
    <div class="">
      <div class="flex gap-4 justify-between w-full bg-gray-800">
        <img :src="image" class="w-20 bg-gray-800" alt="">
        <div class="border-b border-gray-600 flex justify-between items-center w-full">
          <div>
            <h3>{{ title }}</h3>
            <span>{{ subtitle }}</span>
          </div>
          <button>Get</button>
        </div>
      </div>
      <p class="my-2 transition-all delay-100" v-if="showParagraph">{{ paragraphe }}</p>
    </div>
  </article>
</template>