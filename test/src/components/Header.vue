<template>
  <div class="background">
    <nav
      class="container mx-auto flex items-center justify-between flex-wrap pt-8 px-6 md:px-10"
    >
      <div class="flex items-center flex-shrink-0 text-black mr-6">
        <transition appear name="fadeDown">
          <a
            class="cursor-pointer inline-block w-8 grow"
            href="/"
            rel="noopener noreferrer"
          >
            <img alt="Logo Icon" class="logo" src="@/assets/svg/logo.svg" />
          </a>
        </transition>
      </div>
      <div class="hidden lg:block lg:inline-flex lg:items-center lg:w-auto">
        <div class="text-sm lg:flex-grow">
          <a
            href="/"
            v-smooth-scroll="{ duration: 1000, offset: 50 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer gt-walsheim-regular text-black hover-link mr-5"
          >
            Home
          </a>
          <a
            href="#discover"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer gt-walsheim-regular text-black hover-link mr-5"
          >
            Discover
          </a>
          <a
            href="#contact"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer gt-walsheim-regular text-black hover-link mr-5"
          >
            Contact Us
          </a>
          <a
            href="#"
            v-smooth-scroll="{ duration: 1000 }"
            class="block mt-4 lg:inline-block lg:mt-0 cursor-pointer gt-walsheim-regular text-black hover-link"
          >
            Register
          </a>
          <div class="search-box">
            <button class="btn-search">
              <img src="@/assets/img/search-icon.png" alt="search" class="icon" />
            </button>
            <input type="text" class="input-search" placeholder="Search" />
          </div>
        </div>
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: "Header"
};
</script>

<style lang="scss" scoped>
.logo {
  width: 100%;
}

.search-box {
  width: fit-content;
  height: fit-content;
  position: relative;
}
.input-search {
  height: 50px;
  width: 70px;
  border-style: none;
  padding: 10px;
  font-size: 18px;
  letter-spacing: 2px;
  outline: none;
  border-radius: 25px;
  transition: all 0.5s ease-in-out;
  background-color: transparent;
  padding-right: 40px;
  color: black;
  position: relative;
  left: 20px;
}
.input-search::placeholder {
  color: transparent;
  font-size: 14px;
  letter-spacing: 2px;
  font-weight: 100;
}
.btn-search {
  width: 50px;
  height: 50px;
  border-style: none;
  font-size: 14px;
  font-weight: bold;
  outline: none;
  cursor: pointer;
  border-radius: 50%;
  position: absolute;
  right: 0px;
  color: #000000;
  background-color: transparent;
  pointer-events: painted;
}
.btn-search:focus ~ .input-search {
  width: 200px;
  border-radius: 0px;
  background-color: transparent;
  border-bottom: 1px solid rgba(0, 0, 0, 0.5);
  transition: all 500ms cubic-bezier(0, 0.11, 0.35, 2);
}
.input-search:focus {
  width: 200px;
  border-radius: 0px;
  background-color: transparent;
  border-bottom: 1px solid rgba(0, 0, 0, 0.5);
  transition: all 500ms cubic-bezier(0, 0.11, 0.35, 2);
}

.icon {
  width: 50%;
  position: relative;
  top: 10px;
  right: 20px;
}
</style>
