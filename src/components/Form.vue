<script></script>

<template>
  <form @submit.prevent class="bg-white p-9 box-shadow rounded-xl">
    <div>
      <div class="relative">
        <input
          type="text"
          name="firstname"
          placeholder="First Name"
          required
          class="flex-1 w-full outline-none text-lg font-semibold placeholder:font-medium transition placeholder:text-grayish-blue text-dark-blue border-[1px] border-grayish-blue focus:border-dark-blue px-6 py-4 rounded-md"
        />
        <img
          src="../assets/icon-error.svg"
          class="w-[27px] h-[27px] absolute top-1/2 transform -translate-y-1/2 right-5"
          alt=""
        />
      </div>
      <p>First Name cannot be empty</p>
    </div>
    <!-- /input-field -->

    <button
      type="submit"
      class="w-full text-center font-medium uppercase text-base bg-primary-green text-white py-5 px-3 rounded-md hover:opacity-70 button-box-shadow transition"
    >
      Claim your free trial
    </button>
  </form>
</template>
