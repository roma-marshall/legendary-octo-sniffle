<template>
  <div class="text-center mx-40 justify-between min-h-screen font-sans">
    <div class="w-2/2 bg-cover">
      <div class="w-2/2">
        <div class="flex flex-col px-24 pt-10">
          <Logo/>
          <div class="pt-20 pb-6">
            <h1 class="text-3xl font-bold tracking-wide leading-loose">
              Hey, Welcome back!
            </h1>
            <span class="text-gray-500">
              Login below via username & password
            </span>
          </div>
          <div class="flex justify-between items-center pt-6">
            <hr class="w-full border-gray-400"/>
            <span class="px-4 font-light tracking-wider text-gray-500">*</span>
            <hr class="w-full border-gray-400"/>
          </div>
          <form action="">
            <div class="pt-6">
              <label for="email" class="font-light">Email</label>
              <div
                  class="flex items-center mt-2 w-full rounded-lg border border-gray-400 transition-all focus-within:shadow-lg focus-within:border-orange-500">
                <div class="flex justify-center items-center pl-6">
                  <Mail class="w-6 h-6 pointer-events-none"/>
                </div>
                <input
                    type="text"
                    name="email"
                    id="email"
                    value="hello@mail.su"
                    class="px-4 py-4.5 w-full focus:outline-none font-light border-0 focus:ring-0"
                />
              </div>
            </div>
            <div class="pt-6">
              <label for="email" class="font-light">Password</label>
              <div
                  class="flex items-center mt-2 w-full rounded-lg border border-gray-400 transition-all focus-within:shadow-lg focus-within:border-orange-500">
                <div class="flex justify-center items-center pl-6">
                  <Password class="w-6 h-6 pointer-events-none"/>
                </div>
                <input
                    type="password"
                    name="password"
                    id="password"
                    placeholder="*********"
                    class="px-4 py-4.5 w-full focus:outline-none font-light border-0 focus:ring-0"
                />
              </div>
            </div>
            <div class="flex justify-between items-center pt-4">
              <div class="flex items-center">
                <input
                    type="checkbox"
                    name="remember"
                    id="remember"
                    class="w-5 h-5 accent-orange-500 bg-white rounded border border-gray-400 focus:outline-none focus:ring-orange-500"
                />
                <label for="remember" class="pl-4 font-light text-gray-900">
                  Remember me
                </label>
              </div>
              <a href="#" class="text-teal-500 hover:text-teal-600">
                Forgot password
              </a>
            </div>
            <div class="pt-8">
              <button
                  type="submit"
                  class="py-4 px-8 w-full text-white bg-orange-500 rounded-lg shadow-lg hover:bg-orange-600 focus-ring-4 focus:ring-red-100 focus:outline-none"
              >
                Sign in
              </button>
            </div>
          </form>
          <div class="pt-4">
            <div class="font-light text-center text-gray-500">
              Not registered yet?
              <a href="#" class="font-normal text-teal-500 hover:text-teal-600">
                Create an Account
              </a>
            </div>
            <div class="flex justify-between items-center pt-14 pb-3">
              <span class="text-gray-500">© {{ currentDate() }} All rights reserved.</span>
              <span class="flex items-center space-x-1">
                <a href="#" class="hover:text-gray-600 text-gray-500">Terms of Service</a>
                <span class="text-gray-500">&#183;</span>
                <a href="#" class="hover:text-gray-600 text-gray-500">Privacy Policy</a>
              </span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Logo from './assets/img/logo.svg'
import Mail from './assets/img/mail.svg'
import Password from './assets/img/password.svg'

export default {
  name: 'App',
  components: {
    Logo,
    Mail,
    Password
  },
  setup() {
    return {
      Logo,
      Mail,
      Password
    }
  },
  methods: {
    currentDate() {
      const current = new Date();
      const date = `${current.getFullYear()}`;
      return date;
    }
  }
};
</script>

<style scoped>

</style>
