<script setup lang="ts">
  import Card from './components/Card.vue'
</script>

<template>
  <main class="bg-gray-900 flex items-center justify-center h-screen w-full">
    <section class="py-5 relative lg:w-1/2 md:w-[70%] w-full shadow rounded-xl bg-gray-800">
      <Card
        image="https://animations.dev/how-i-use-framer-motion/how-i-code-animations/pirate.png"
        title="Pirates in the jungle"
        subtitle="Find the treasure."
        paragraphe="You are a pirate and you have to find the treasure in the jungle. But be careful, there are traps and wild animals. Some filler text to make it longer. Maybe even longer, because it looks better."
      />
      <Card
        image="https://animations.dev/how-i-use-framer-motion/how-i-code-animations/boy.webp"
        title="Lost in the mountains"
        subtitle="Be careful."
        paragraphe="You are lost in the mountains and you have to find your way home. But be careful, there are dangerous animals and you can get lost."
      />
      <Card
        image="https://animations.dev/how-i-use-framer-motion/how-i-code-animations/pirate.png"
        title="Pirates in the jungle"
        subtitle="Find the treasure."
        paragraphe="You are a pirate and you have to find the treasure in the jungle. But be careful, there are traps and wild animals. Some filler text to make it longer. Maybe even longer, because it looks better."
      />
      <Card
        image="https://animations.dev/how-i-use-framer-motion/how-i-code-animations/boy.webp"
        title="Lost in the mountains"
        subtitle="Be careful."
        paragraphe="You are lost in the mountains and you have to find your way home. But be careful, there are dangerous animals and you can get lost."
      />
    </section>
  </main>
</template>

<style scoped>

</style>
