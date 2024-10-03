<script setup>
  import FooterBase from './components/FooterBase.vue'
  import HeaderBase from './components/HeaderBase.vue'
  import NavigationBase from './components/NavigationBase.vue'
  import PopupBase from './components/PopupBase.vue'
  import SectionAbout from './components/SectionAbout.vue'
  import SectionBook from './components/SectionBook.vue'
  import SectionFeatures from './components/SectionFeatures.vue'
  import SectionStories from './components/SectionStories.vue'
  import SectionTours from './components/SectionTours.vue'
</script>

<template>
  <NavigationBase />
  <HeaderBase />

  <main>
    <SectionAbout />
    <SectionFeatures />
    <SectionTours />
    <SectionStories />
    <SectionBook />
  </main>

  <FooterBase />
  <PopupBase />
</template>
