<script>
export default {
  name: 'Attribution',
};
</script>

<template>
  <div
    id="attribution"
    class="font-medium text-base text-center max-w-[470px] w-full px-1 py-3 rounded-md mx-auto fixed bottom-5 left-1/2 -translate-x-1/2"
  >
    Challenge by
    <a
      class="hover:underline"
      href="https://www.frontendmentor.io/challenges/intro-component-with-signup-form-5cf91bd49edda32581d28fd1"
      target="_blank"
    >
      Frontend Mentor
    </a>
    . Coded by
    <a
      class="hover:underline"
      href="https://www.frontendmentor.io/profile/sam4web"
      target="_blank"
    >
      Sam4web </a
    >.
  </div>
</template>

<style scoped>
#attribution {
  background-color: hsla(0, 0%, 100%, 0.851);
}

#attribution a {
  color: hsl(228, 45%, 44%);
}
</style>
