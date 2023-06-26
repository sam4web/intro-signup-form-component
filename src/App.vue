<script>
import Form from './components/Form.vue';
import Notification from './components/Notification.vue';

export default {
  components: {
    Form,
    Notification,
  },
};
</script>

<template>
  <div id="page-wrapper" class="w-full h-screen flex jus items-center">
    <section class="max-w-7xl w-full mx-auto md:px-6 px-4 flex">
      <div class="flex-1">
        <h1 class="text-white font-bold text-5xl leading-[1.12] mb-9">
          Learn to code by
          <br />
          watching others
        </h1>
        <p class="text-white text-lg">
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
  </div>
</template>
