<template>
  <div class="overflow-x-hidden">
    <Header />
    <div class="background--alt">
      <div class="container mx-auto flex md:min-h-screen">
        <div class="flex">
          <div class="inline-flex flex-col md:flex-row flex-no-wrap md:items-center">
            <div class="md:w-1/2 px-6 md:px-12 flex flex-col md:items-start">
              <h1 class="mt-12 lg:text-3xl max-w-md gt-walsheim-medium leading-tight">
                BOOKED TOOLS
                <span
                  class="mt-4 text-base lg:text-lg max-w-md open-sans-regular leading-snug"
                >
                  enables you to create Interactive Advertisement
                </span>
              </h1>
              <transition appear name="fade">
                <div class="button">
                  <button type="submit" form="my-form">What is it?</button>
                </div>
              </transition>
            </div>
            <div class="md:w-1/2 md:px-16 mt-8 block md:hidden">
              <transition appear name="fade">
                <img class="mt-8 block md:hidden" src="@/assets/svg/aboutus.svg" />
              </transition>
            </div>
            <div class="md:w-1/2 md:px-16 hidden md:block">
              <transition appear name="fade">
                <img class="hidden md:block" src="@/assets/svg/landing-image.svg" />
              </transition>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div class="container mx-auto flex flex-col items-center mt-24 mb-24 md:mb-32">
      <h1 class="mt-12 lg:text-3xl max-w-md gt-walsheim-medium leading-tight">
        Please Login to start using
      </h1>
      <h1 class="mt-12 lg:text-5xl max-w-md gt-walsheim-medium leading-tight">
        BOOKED TOOL
      </h1>
      <Login />
    </div>
    <div class="flex">
      <div class="container mx-auto flex flex-col items-center mt-24 mb-24">
        <div class="w-5/6 md:w-3/4">
          <img src="@/assets/img/illustrations/done_sunday.jpg" />
        </div>
        <h1
          class="mt-16 text-center text-3xl md:text-3xl lg:text-4xl gt-walsheim-medium"
          v-scroll-reveal="{ delay: 500, distance: '15%' }"
        >
          Booked Tool enables you to create Interactive Advertisement
        </h1>
      </div>
    </div>
    <div id="discover" class="flex px-8 md:px-0 background--alt">
      <div class="mx-auto flex flex-col flex-no-wrap items-center mt-24 mb-24">
        <h1 class="text-2xl md:text-4xl text-center gt-walsheim-medium leading-tight">
          DISCOVER <br />BOOKED TOOLS
        </h1>
        <p
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >
          Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
          incididunt ut labore et dolore magna aliqua..
        </p>
        <div
          class="mt-4 text-center text-base md:text-xl lg:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >
          <Tab />
        </div>
      </div>
    </div>
    <div id="contact" class="flex px-10 md:px-0">
      <div class="container mx-auto flex flex-col items-center mt-24 mb-24 md:mb-32">
        <h1 class="text-2xl md:text-4xl gt-walsheim-medium leading-tight">
          Get In Touch
        </h1>
        <p
          class="mt-4 text-center text-base md:text-xl open-sans-regular leading-snug md:max-w-4xl md:px-32"
        >
          Want to get in touch? We'd love to hear from you. Here's how you can reach us...
        </p>
        <ContactUs />
      </div>
    </div>
    <div id="community" class="flex">
      <div class="container mx-auto flex flex-col px-6 md:px-0 items-center mt-24 mb-24">
        <div class="w-5/6 md:w-3/4 background--illustration">
          <img src="@/assets/img/illustrations/done_sunday.jpg" alt="" />
        </div>
        <h1
          class="mt-16 text-center md:text-left text-3xl md:text-4xl gt-walsheim-medium leading-tight"
          v-scroll-reveal="{ delay: 500, distance: '15%' }"
        >
          Lorem ipsum dolor sit amet, consectetur adipiscing elit.
        </h1>
        <p
          class="mt-4 text-center text-base md:text-xl open-sans-regular leading-snug px-5 md:max-w-5xl md:px-40"
          v-scroll-reveal="{ delay: 500, distance: '15%' }"
        >
          Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut
          aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in
          voluptate velit esse cillum dolore eu fugiat nulla pariatur. Excepteur sint
          occaecat cupidatat non proident, sunt in culpa qui officia deserunt mollit anim
          id est laborum.
        </p>
      </div>
    </div>
    <Footer />
  </div>
</template>

<script>
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Tab from "@/components/TabMenu.vue";
import ContactUs from "@/components/ContactUs.vue";
import Login from "@/components/Login.vue";

export default {
  name: "Home",
  components: {
    Header,
    Footer,
    ContactUs,
    Login,
    Tab,
  },
};
</script>

<style lang="scss" scoped>
.button {
  cursor: pointer;
  color: white;
  font-size: 1.8rem;
  font-weight: 500;
  display: block;
  margin: 2% auto;
  padding: 1.5% 5%;
  margin-left: 0px;
  border: none;
  border-radius: 5px;
  line-height: 28px;
  background: rgb(255, 154, 98);
  background: linear-gradient(
    90deg,
    rgba(255, 154, 98, 1) 0%,
    rgba(255, 114, 121, 1) 50%,
    rgba(255, 68, 147, 1) 100%
  );
}
</style>
