<template>
  <div
    class="relative flex items-top justify-center min-h-screen bg-gray-100 sm:items-center sm:pt-0"
  >
    <Tutorial />
    <p>
      <nuxt-link :to="localePath('index')">{{ $t('home') }}</nuxt-link>
      <nuxt-link :to="localePath('/')">{{ $t('home') }}</nuxt-link>
      <nuxt-link :to="localePath('index', 'en')">Homepage in English</nuxt-link>
      <nuxt-link :to="localePath('/app/profile')"
        >Route by path to: {{ $t('Profile') }}</nuxt-link
      >
      <nuxt-link :to="localePath('app-profile')"
        >Route by name to: {{ $t('Profile') }}</nuxt-link
      >
      <!-- <nuxt-link
      :to="
        localePath({ name: 'category-slug', params: { slug: category.slug } })
      "
    >
      {{ category.title }}
    </nuxt-link> -->
      <!-- It's also allowed to omit 'name' and 'path'. -->
      <!-- <nuxt-link :to="localePath({ params: { slug: 'ball' } })">{{
      category.title
    }}</nuxt-link> -->
    </p>
    <footer>
      <p>
        <nuxt-link :to="switchLocalePath('en')">English</nuxt-link>
        <nuxt-link :to="switchLocalePath('fr')">Français</nuxt-link>
        <nuxt-link :to="switchLocalePath('es')">Estonia</nuxt-link>
      </p>
    </footer>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
}
</script>
