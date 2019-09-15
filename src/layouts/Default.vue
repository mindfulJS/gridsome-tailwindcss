<template>
  <div class="layout">
    <header class="header">
      <strong>
        <g-link to="/">{{ $static.metaData.siteName }}</g-link>
      </strong>
      <nav class="nav">
        <g-link class="nav__link" to="/">
          <NavButton>Home</NavButton>
        </g-link>
        <g-link class="nav__link" to="/about"><NavButton>About</NavButton></g-link>
      </nav>
    </header>
    <slot/>
  </div>
</template>

<static-query>
query {
  metaData {
    siteName
  }
}
</static-query>

<style src="../main.css" />

<script>
import NavButton from "../components/NavButton.vue";

export default {
  name: "App",
  components: {
    NavButton
  }
};
</script>

