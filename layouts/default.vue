<template>
  <div class="default-layout">
    <TheHeader />
    <Nuxt />
    <TheFooter />
  </div>
</template>

<script>
import TheHeader from "../components/layouts/TheHeader"
import TheFooter from "../components/layouts/TheFooter"

export default {
  name: "DefaultLayout",
  components: { TheHeader, TheFooter },
}
</script>

<style lang="scss">
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: $font-family;
  text-decoration: none;
  color: inherit;

  &:hover {
    color: inherit;
  }
}

html,
body,
#__nuxt,
#__layout {
  width: 100%;
  min-height: 100%;
  background-color: $color-default-bg;
}

.default-layout {
  display: flex;
  width: 100%;
  min-height: 100%;
  flex-direction: column;

  main {
    display: flex;
    flex-grow: 1;
    flex-direction: column;
  }
}
</style>
