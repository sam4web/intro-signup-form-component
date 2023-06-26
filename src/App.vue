<script>
import Form from './components/Form.vue';
import Notification from './components/Notification.vue';
import Attribution from './components/Attribution.vue';

export default {
  name: 'App',
  components: {
    Form,
    Notification,
    Attribution,
  },
};
</script>

<template>
  <div
    id="page-wrapper"
    class="w-full md:h-screen h-fit flex items-center py-9"
  >
    <section
      class="max-w-7xl w-full mx-auto md:px-6 px-3 flex gap-6 md:flex-row flex-col md:items-center"
    >
      <div class="flex-1 max-w-2xl w-full mx-auto md:text-left text-center">
        <h1
          class="text-white font-bold md:text-5xl text-3xl leading-snug md:mb-9 mb-5"
        >
          Learn to code by
          <br class="md:block hidden" />
          watching others
        </h1>
        <p class="text-white md:text-lg text-base">
          See how experienced developers solve problem in real-time. Watching
          scripted tutorials is great, but understanding how developers think is
          invaluable.
        </p>
      </div>
      <!-- /content -->

      <div class="flex-1">
        <Notification />
        <Form />
      </div>
      <!-- form-container -->
    </section>
    <Attribution />
  </div>
</template>
