<script setup>
import { useDark, useToggle } from '@vueuse/core';

const isDark = useDark();
const toggleDark = useToggle(isDark);
</script>
<template>
  <button
      @click="toggleDark()"
      class="fixed right-[30px] top-[30px] z-[99] flex justify-center items-center w-[48px] h-[48px] rounded-full transition-all duration-300 ease-linear outline-0 cursor-pointer bg-dark dark:bg-white"
  >
        <span class="icon block dark:hidden">
          <svg class="stroke-white w-[17px]" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M21.752 15.002A9.718 9.718 0 0118 15.75c-5.385 0-9.75-4.365-9.75-9.75 0-1.33.266-2.597.748-3.752A9.753 9.753 0 003 11.25C3 16.635 7.365 21 12.75 21a9.753 9.753 0 009.002-5.998z" />
          </svg>
        </span>
    <span class="icon hidden dark:block">
          <svg class="stroke-dark w-[17px]" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" d="M12 18v-5.25m0 0a6.01 6.01 0 001.5-.189m-1.5.189a6.01 6.01 0 01-1.5-.189m3.75 7.478a12.06 12.06 0 01-4.5 0m3.75 2.383a14.406 14.406 0 01-3 0M14.25 18v-.192c0-.983.658-1.823 1.508-2.316a7.5 7.5 0 10-7.517 0c.85.493 1.509 1.333 1.509 2.316V18" />
          </svg>
        </span>
  </button>
  <div class="w-full">
    <div class="flex flex-wrap h-screen overflow-y-auto relative">
      <!-- left content end -->
      <div class="lg:w-6/12 md:w-full lg:bg-[#fff] md:bg-[#F5F9FF] lg:p-0 md:p-[40px] dark:bg-dark">
        <div
            class="login-left py-[40px] xxl:px-[120px] xl:px-[80px] lg:px-[40px] md:px-[40px] px-[20px] bg-[#fff] lg:rounded-0 rounded-[10px] dark:bg-dark">
          <!-- login heading start -->
          <div class="login-left-heading md:text-left text-center">
            <!-- logo start -->
            <div class="logo mb-[40px]">
              <router-link to="/">
                <img class="inline-block w-[120px] hidden dark:block" src="/assets/img/logo/logo-s.png" alt="logo">
                <img class="inline-block w-[120px] block dark:hidden" src="/assets/img/logo/logo-dark.png" alt="logo">
              </router-link>
            </div>
            <!-- logo end -->
            <h1 class="text-dark xxl:text-5xl xl:text-4xl text-[24px] font-bold tracking[-0.24px] mb-[8px] dark:text-white">
              Exclusive Dashboard
              Tour</h1>
            <p class="lg:w-10/12 md:w-9/12 text-[18px] leading-[27px] text-dark dark:text-white/70">Get access to exclusive tour of
              our platform
              within 10 seconds, by simply submitting the following
              information.</p>
          </div>
          <!-- login heading end -->
          <!-- login form start -->
          <form action="#" class="login-form mt-[48px]">
            <!-- google & facebook start -->
            <div class="flex xl:flex-nowrap lg:flex-wrap md:flex-nowrap flex-wrap items-center gap-[20px]">
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <a href="#"
                   class="flex justify-center items-center py-[5px] px-[15px] bg-[#0B9201]/20 border border-[#0B9201] text-dark xl:text-[16px] text-[14px] lg:h-[70px] h-[60px] rounded-[10px] transition duration-300 ease-linear hover:bg-[#0B9201]/10 hover:border-[#0B9201]/10 hover:text-[#0B9201] dark:bg-[#0B9201]/50 dark:text-white">
                  <img class="mr-[15px] xl:w-[22px] w-[15px]" src="/assets/img/icon/google.svg" alt="google">
                  Login with Google
                </a>
              </div>
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <a href="#"
                   class="flex justify-center items-center py-[5px] px-[15px] bg-[#635bff]/20 border border-[#635bff] text-dark xl:text-[16px] text-[14px] lg:h-[70px] h-[60px] rounded-[10px] transition duration-300 ease-linear hover:bg-[#635bff]/10 hover:border-[#635bff]/10 hover:text-[#635bff] dark:bg-[#635bff]/50 dark:text-white">
                  <img class="mr-[15px] xl:w-[22px] w-[15px]" src="/assets/img/icon/facebook.svg" alt="google">
                  Login with Facebook
                </a>
              </div>
            </div>
            <!-- google & facebook end -->
            <div class="separator flex items-center justify-center my-[40px]">
              <div class="bar flex-1 border-t border-dark/20 dark:border-white/20"></div>
              <span class="text-dark text-[14px] text-center w-[30px] mx-[10px] dark:text-white">OR</span>
              <div class="bar flex-1 border-t border-dark/20 dark:border-white/20"></div>
            </div>
            <!-- inputs start -->
            <div
                class="flex xl:flex-nowrap lg:flex-wrap md:flex-nowrap flex-wrap items-center xl:gap-[20px] lg:gap-0 md:gap-[20px]">
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="input-wrap mb-[20px]">
                  <input type="text" placeholder="First Name"
                         class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 focus:border-[#0B9201]">
                </div>
              </div>
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="input-wrap mb-[20px]">
                  <input type="text" placeholder="Last Name"
                         class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 focus:border-[#0B9201]">
                </div>
              </div>
            </div>
            <div
                class="flex xl:flex-nowrap lg:flex-wrap md:flex-nowrap flex-wrap items-center xl:gap-[20px] lg:gap-0 md:gap-[20px]">
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="input-wrap mb-[20px]">
                  <input type="text" placeholder="Email Address"
                         class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 focus:border-[#0B9201]">
                </div>
              </div>
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="select-wrap mb-[20px] relative">
                  <select
                      class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 appearance-none focus:border-[#0B9201]">
                    <option value="">Select Country</option>
                    <option value="">Afghanistan</option>
                    <option value="">Bahamas</option>
                    <option value="">Bangladesh</option>
                    <option value="">Canada</option>
                    <option value="">Chili</option>
                  </select>
                  <div class="icon absolute right-[20px] top-[50%] translate-y-[-50%] pointer-events-none">
                    <svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5"
                         stroke="currentColor" class="w-6 h-6">
                      <path stroke-linecap="round" stroke-linejoin="round" d="M19.5 8.25l-7.5 7.5-7.5-7.5"/>
                    </svg>
                  </div>
                </div>
              </div>
            </div>
            <div
                class="flex xl:flex-nowrap lg:flex-wrap md:flex-nowrap flex-wrap items-center xl:gap-[20px] lg:gap-0 md:gap-[20px]">
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="input-wrap mb-[20px]">
                  <input type="password" placeholder="Password"
                         class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 focus:border-[#0B9201]">
                </div>
              </div>
              <div class="xl:w-6/12 lg:w-full md:w-6/12 w-full">
                <div class="input-wrap mb-[20px]">
                  <input type="password" placeholder="Confirm Password"
                         class="w-full lg:h-[70px] h-[60px] px-[25px] bg-[#fff] text-dark border border-dark/20 rounded-[10px] outline-0 focus:border-[#0B9201]">
                </div>
              </div>
            </div>
            <div class="input-btn mt-[40px] mb-[20px] text-center">
              <button
                  class="inline-block lg:h-[70px] h-[60px] py-[5px] md:px-[112px] px-[80px] bg-[#0B9201] text-[#fff] xl:text-[24px] text-[18px] border border-[#0B9201] rounded-[10px] uppercase focus:border-[#0B9201]">
                Register
              </button>
            </div>
            <div class="link-wrap mb-[40px] text-center">
              <router-link to="/" class="text-[18px] text-[#0B9201] hover:underline dark:text-primary">Yes, take me to dashboard</router-link>
            </div>
            <div class="info mb-[30px] text-center">
              <p class="text-[18px] mb-[16px] dark:text-white/70">
                Already have an account?
                <router-link to="/login" class="text-[#0B9201] hover:underline dark:text-primary">Login Now</router-link>
              </p>
              <p class="text-[18px] dark:text-white/70">
                Copyright © admin 2022.
              </p>
            </div>
            <!-- inputs end -->
          </form>
          <!-- left content end -->
        </div>
      </div>
      <!-- left content end -->

      <!-- right content start -->
      <div class="w-6/12 bg-[#0B9201] bg-cover bg-no-repeat lg:flex hidden flex-wrap items-center justify-center"
           :style="{backgroundImage:'url(/assets/img/bg/white-pattern.png)'}">
        <div class="thumb flex flex-wrap justify-center w-[85%]">
          <img src="/assets/img/thumb/thumb-1.png" alt="">
          <h1 class="text-white xl:text-5xl lg:text-3xl text-center font-bold w-[528px] mt-[50px]">Take an exclusive
            dashboard tour and
            explore</h1>
        </div>
      </div>
      <!-- right content end -->
    </div>
  </div>
</template>

<script>
export default {
  name: "Register",
  data() {
    return {}
  }
}
</script>

<style scoped>

</style>