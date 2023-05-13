<template>
  <Menu as="div" class="relative inline-block text-left">
    <div>
      <MenuButton
        class="inline-flex w-full justify-center items-center px-4 pl-5 py-2 text-sm text-black font-semibold rounded-full"
        :class="background"
      >
        <span>
          <img src="../assets/images/icons/eng-flag.png" class="mr-2 w-6 h-6" />
        </span>
        <span>Language</span>
        <svg
          width="30"
          height="30"
          viewBox="0 0 60 60"
          fill="none"
          xmlns="http://www.w3.org/2000/svg"
        >
          <path
            d="M42.5012 22.9252C42.0328 22.4596 41.3992 22.1982 40.7387 22.1982C40.0782 22.1982 39.4446 22.4596 38.9762 22.9252L30.0012 31.7752L21.1512 22.9252C20.6828 22.4596 20.0492 22.1982 19.3887 22.1982C18.7283 22.1982 18.0946 22.4596 17.6262 22.9252C17.3919 23.1576 17.2059 23.4341 17.079 23.7388C16.9521 24.0434 16.8867 24.3702 16.8867 24.7002C16.8867 25.0303 16.9521 25.357 17.079 25.6617C17.2059 25.9663 17.3919 26.2428 17.6262 26.4752L28.2262 37.0752C28.4586 37.3095 28.7351 37.4955 29.0398 37.6225C29.3444 37.7494 29.6712 37.8147 30.0012 37.8147C30.3312 37.8147 30.658 37.7494 30.9627 37.6225C31.2673 37.4955 31.5438 37.3095 31.7762 37.0752L42.5012 26.4752C42.7355 26.2428 42.9215 25.9663 43.0484 25.6617C43.1754 25.357 43.2407 25.0303 43.2407 24.7002C43.2407 24.3702 43.1754 24.0434 43.0484 23.7388C42.9215 23.4341 42.7355 23.1576 42.5012 22.9252Z"
            fill="#74BDCB"
          />
        </svg>
      </MenuButton>
    </div>

    <transition
      enter-active-class="transition duration-100 ease-out"
      enter-from-class="transform scale-95 opacity-0"
      enter-to-class="transform scale-100 opacity-100"
      leave-active-class="transition duration-75 ease-in"
      leave-from-class="transform scale-100 opacity-100"
      leave-to-class="transform scale-95 opacity-0"
    >
      <MenuItems
        class="z-10 absolute right-0 mt-2 w-40 origin-top-right divide-y divide-gray-100 rounded-md bg-white shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
      >
        <div class="px-1 py-1">
          <MenuItem v-slot="{ active }">
            <button
              :class="[
                active ? 'bg-body' : 'text-black',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
            >
              English
            </button>
          </MenuItem>
          <MenuItem v-slot="{ active }">
            <button
              :class="[
                active ? 'bg-body' : 'text-black',
                'group flex w-full items-center rounded-md px-2 py-2 text-sm',
              ]"
            >
              German
            </button>
          </MenuItem>
        </div>
      </MenuItems>
    </transition>
  </Menu>
</template>
  
  <script>
import { Menu, MenuButton, MenuItems, MenuItem } from "@headlessui/vue";
export default {
  name: "LanguageDropdown",
  components: {
    Menu,
    MenuButton,
    MenuItems,
    MenuItem,
  },
  props: {
    background: String,
  },
};
</script>
  