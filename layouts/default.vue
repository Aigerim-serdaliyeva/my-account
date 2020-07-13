<template>
  <div>
      <Header class="d-none d-md-flex" />
      <HeaderMobile class="d-md-none" />
      <Nuxt />
  </div>
</template>

<script>
import Header from '../components/header/Header';
import HeaderMobile from '../components/header/HeaderMobile';

export default {
  components: {
    Header,
    HeaderMobile
  }
}
</script>

<style>
</style>
