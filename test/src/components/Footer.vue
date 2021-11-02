<template>
  <div class="pt-24 pb-20 md:pb-16 bg-white p-8 background--alt">
    <div class="container mx-auto text-left opacity-100 text-sm lg:px-4">
      <div
        class="flex flex-col justify-center items-start content-start lg:flex-row mb-4"
      >
        <div class="mb-6 md:mb-0 sm:w-1/4 h-auto">
          <a
            v-scroll-reveal="{ delay: 1000, distance: '5%' }"
            class="cursor-pointer inline-block w-8"
            href="/"
            rel="noopener noreferrer"
          >
            <img alt="Logo Icon" class="w-8 grow" src="@/assets/svg/logo.svg" />
          </a>
          <p
            class="mt-32 text-left gt-walsheim-regular text-grey text-sm opacity-50 hidden lg:block"
          >
            © Booked Tool
          </p>
        </div>
        <div class="sm:w-1/4 h-auto sm:mt-0 mt-8">
          <div class="gt-walsheim-medium text-lg text-grey-darkest mb-4">Booked Tool</div>
          <ul class="list-reset leading-normal cursor-pointer">
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                rel="noopener noreferrer"
                >Download the iOS app</a
              >
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                rel="noopener noreferrer"
                >Download the Android app</a
              >
            </li>
            <li class="mb-4 md:mb-2">
              <a
                class="link open-sans-regular text-grey-darker hover-link"
                rel="noopener noreferrer"
                >Learn more about Booked Tool</a
              >
            </li>
          </ul>
        </div>
        <div class="sm:w-1/4 h-auto mt-8 lg:mt-0">
          <div class="gt-walsheim-medium text-lg text-grey-darkest mb-4">Help</div>
          <h1>
            Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor
            incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis
            nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.
            Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore
            eu fugiat nulla pariatur. Excepteur sint occaecat cupidatat non proident, sunt
            in culpa qui officia deserunt mollit anim id est laborum.
          </h1>
        </div>
        <div>
          <transition appear name="fade">
            <div class="mt-12 mt-4 lg:mt-0">
              <a
                class="opacity-100 inline-block w-8 mr-6 md:mr-4 grow"
                target="_blank"
                rel="noopener noreferrer"
                title="GitHub"
              >
                <img alt="Github Icon" class="w-8" src="@/assets/svg/instagram.svg" />
              </a>
              <a
                class="opacity-100 inline-block w-8 mr-6 md:mr-4 grow"
                target="_blank"
                rel="noopener noreferrer"
                title="Twitter"
              >
                <img
                  alt="Twitter Icon"
                  class="w-14"
                  src="@/assets/svg/logo-twitter.svg"
                />
              </a>
              <a
                class="opacity-100 inline-block w-8 mr-6 md:mr-4 grow"
                target="_blank"
                rel="noopener noreferrer"
                title="Facebook"
              >
                <img alt="Discord Icon" class="w-8" src="@/assets/svg/facebook.svg" />
              </a>
            </div>
          </transition>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Footer",
};
</script>
