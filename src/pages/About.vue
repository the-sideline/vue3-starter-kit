<template>
  <div class="about">
    <h1>About Vue 3 Starter Kit</h1>
    <div class="features">
      <h2>Features</h2>
      <ul>
        <li>Vue 3 with Composition API</li>
        <li>TypeScript support</li>
        <li>Vite for fast development</li>
        <li>Vue Router with history mode</li>
        <li>Pinia for state management</li>
        <li>ESLint and Prettier for code quality</li>
      </ul>
    </div>

    <div class="pages">
      <h2>Available Pages</h2>
      <ul>
        <li><strong>Home:</strong> Demonstrates Pinia counter store with BaseButton component</li>
        <li><strong>Welcome:</strong> Shows the TheWelcome component with ecosystem links</li>
        <li><strong>About:</strong> This page with project information</li>
      </ul>
    </div>

    <div class="components">
      <h2>Components</h2>
      <ul>
        <li><strong>HelloWorld:</strong> Welcome message component (used in header)</li>
        <li><strong>TheWelcome:</strong> Ecosystem showcase component (used in Welcome page)</li>
        <li><strong>BaseButton:</strong> Reusable button component (used in Home page)</li>
        <li><strong>WelcomeItem:</strong> Individual welcome item component</li>
        <li><strong>Icon Components:</strong> Various SVG icon components</li>
      </ul>
    </div>
  </div>
</template>

<script setup lang="ts">
// About page logic here
</script>

<style scoped>
.about {
  padding: 2rem;
  max-width: 800px;
  margin: 0 auto;
}

.features,
.pages,
.components {
  margin-top: 2rem;
}

.features ul,
.pages ul,
.components ul {
  list-style-type: none;
  padding: 0;
}

.features li,
.pages li,
.components li {
  padding: 0.5rem 0;
  border-bottom: 1px solid #eee;
}

.features li:last-child,
.pages li:last-child,
.components li:last-child {
  border-bottom: none;
}

@media (min-width: 1024px) {
  .about {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
}
</style>
