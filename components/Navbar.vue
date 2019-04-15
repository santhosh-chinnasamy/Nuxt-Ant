<template>
  <div>
    <a-menu v-model="current" mode="horizontal">
      <a-menu-item key="home">
        <nuxt-link to="/">
          <a-icon type="home"/>Home
        </nuxt-link>
      </a-menu-item>

      <a-menu-item key="about">
        <nuxt-link to="/about">
          <a-icon type="info-circle"/>About
        </nuxt-link>
      </a-menu-item>

      <a-menu-item key="wiki">
        <a
          href="https://en.wikipedia.org/wiki/Dennis_Ritchie"
          target="_blank"
          rel="noopener noreferrer"
        >
          Wiki
          <a-icon type="export"/>
        </a>
      </a-menu-item>
    </a-menu>
  </div>
</template>




<script>
export default {
  data() {
    return {
      current: ['home']
    }
  }
}
</script>
