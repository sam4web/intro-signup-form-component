<template>
  <form
    @submit.prevent="handleSubmit"
    class="bg-white py-7 px-5 md:p-5 md:py-7 lg:p-9 box-shadow rounded-xl max-w-2xl mx-auto w-full"
    novalidate
  >
    <div class="mb-5">
      <div class="relative mb-[6px]">
        <input
          type="text"
          name="firstname"
          placeholder="First Name"
          v-model="firstname"
          class="input-field"
          :class="{ 'error-input': errors?.firstname }"
        />

        <img
          v-if="errors?.firstname"
          src="../assets/icon-error.svg"
          class="w-[27px] h-[27px] absolute top-1/2 transform -translate-y-1/2 right-5"
          alt=""
        />
      </div>

      <p class="error-message" v-if="errors?.firstname">
        {{ errors?.firstname }}
      </p>
    </div>
    <!-- /input-field -->

    <div class="mb-5">
      <div class="relative mb-[6px]">
        <input
          type="text"
          name="lastname"
          placeholder="Last Name"
          v-model="lastname"
          class="input-field"
          :class="{ 'error-input': errors?.lastname }"
        />

        <img
          v-if="errors?.lastname"
          src="../assets/icon-error.svg"
          class="w-[27px] h-[27px] absolute top-1/2 transform -translate-y-1/2 right-5"
          alt=""
        />
      </div>

      <p class="error-message" v-if="errors?.lastname">
        {{ errors?.lastname }}
      </p>
    </div>
    <!-- /input-field -->

    <div class="mb-5">
      <div class="relative mb-[6px]">
        <input
          type="email"
          name="email"
          placeholder="Email Address"
          v-model="email"
          class="input-field"
          :class="{ 'error-input': errors?.email }"
        />

        <img
          v-if="errors?.email"
          src="../assets/icon-error.svg"
          class="w-[27px] h-[27px] absolute top-1/2 transform -translate-y-1/2 right-5"
          alt=""
        />
      </div>

      <p class="error-message" v-if="errors?.email">
        {{ errors?.email }}
      </p>
    </div>
    <!-- /input-field -->

    <div class="mb-5">
      <div class="relative mb-[6px]">
        <input
          type="password"
          name="password"
          placeholder="Password"
          autocomplete="off"
          v-model="password"
          class="input-field"
          :class="{ 'error-input': errors?.password }"
        />

        <img
          v-if="errors?.password"
          src="../assets/icon-error.svg"
          class="w-[27px] h-[27px] absolute top-1/2 transform -translate-y-1/2 right-5"
          alt=""
        />
      </div>

      <p class="error-message" v-if="errors?.password">
        {{ errors?.password }}
      </p>
    </div>
    <!-- /input-field -->

    <button type="submit" class="button">Claim your free trial</button>

    <p class="mt-5 font-normal text-sm text-center text-grayish-blue">
      By clicking the button, you are agreeing to our
      <a href="#" class="hover:underline text-primary-red font-bold"
        >Terms and Services</a
      >
    </p>
  </form>
</template>

<script>
export default {
  name: 'Form',
  data() {
    return {
      firstname: '',
      lastname: '',
      email: '',
      password: '',
      errors: null,
    };
  },
  methods: {
    handleSubmit(e) {
      const errors = {};
      if (!this.firstname) errors.firstname = 'First Name cannot be empty';

      if (!this.lastname) errors.lastname = 'Last Name cannot be empty';

      if (!this.email) errors.email = 'Email is required';
      else if (!/^[^@]+@\w+(\.\w+)+\w$/.test(this.email))
        errors.email = 'Looks like this is not an email';

      if (!this.password) errors.password = 'Password cannot be empty';

      this.errors = errors;
    },
  },
};
</script>
