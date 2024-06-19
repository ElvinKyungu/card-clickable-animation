<script setup lang="ts">
import gsap from 'gsap'
import { ref } from 'vue'
const props = defineProps({
  image: String,
  title: String,
  subtitle: String,
  paragraphe: String
})
const showParagraph = ref(false)

const handleCardClick = (event: Event) => {
  const cardElement = event.currentTarget as HTMLElement
  showParagraph.value = !showParagraph.value
}

</script>
<template>
  <article
    @click="handleCardClick"
    class="
      px-5 py-2 bg-gray-800 cursor-pointer transition-colors text-white 
      rounded-xl lg:mx-24 md:mx-16 mx-5
    "
  >
    <div class="">
      <div class="flex gap-4 justify-between w-full bg-gray-800">
        <img :src="image" class="w-20 bg-gray-800 rounded-2xl" alt="">
        <div class="border-b border-gray-600 flex justify-between items-center w-full">
          <div>
            <h3 class="font-semibold mb-1">{{ title }}</h3>
            <span class="font-thin">{{ subtitle }}</span>
          </div>
          <button class="py-1 px-2 rounded-xl bg-indigo-500/40 text-xs">Get</button>
        </div>
      </div>
      <p class="my-2 transition-all delay-100" v-if="showParagraph">
        {{ paragraphe }}
      </p>
    </div>
  </article>
</template>