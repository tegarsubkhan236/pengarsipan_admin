<script>
  import { link } from "svelte-routing";
  // library for creating dropdown menu appear on click
  import { createPopper } from "@popperjs/core";

  // core components
  let dropdownPopoverShow = false;

  let btnDropdownRef;
  let popoverDropdownRef;

  const toggleDropdown = (event) => {
    event.preventDefault();
    if (dropdownPopoverShow) {
      dropdownPopoverShow = false;
    } else {
      dropdownPopoverShow = true;
      createPopper(btnDropdownRef, popoverDropdownRef, {
        placement: "bottom-start",
      });
    }
  };
</script>

<div>
  <a
    class="hover:text-gray-600 text-gray-800 px-3 py-2 flex items-center text-xs uppercase font-bold"
    href="#pablo"
    bind:this={btnDropdownRef}
    on:click={toggleDropdown}>
    Demo Pages
  </a>
  <div
    bind:this={popoverDropdownRef}
    class="bg-white text-base z-50 float-left py-2 list-none text-left rounded shadow-lg min-w-48 {dropdownPopoverShow ? 'block' : 'hidden'}">
    <span
      class="text-sm pt-2 pb-0 px-4 font-bold block w-full whitespace-no-wrap bg-transparent text-gray-500">
      User Layout
    </span>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Landing
    </a>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Main Collection
    </a>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Child Collection
    </a>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Contents
    </a>
    <div class="h-0 mx-4 my-2 border border-solid border-gray-200" />
    <span
      class="text-sm pt-2 pb-0 px-4 font-bold block w-full whitespace-no-wrap bg-transparent text-gray-500">
      Admin Layout
    </span>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Admin Dashboard
    </a>
    <div class="h-0 mx-4 my-2 border border-solid border-gray-200" />
    <span
      class="text-sm pt-2 pb-0 px-4 font-bold block w-full whitespace-no-wrap bg-transparent text-gray-500">
      Author Layout
    </span>
    <a
      use:link
      href="/admin/dashboard"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Author Dashboard
    </a>
    <div class="h-0 mx-4 my-2 border border-solid border-gray-200" />
    <span
      class="text-sm pt-2 pb-0 px-4 font-bold block w-full whitespace-no-wrap bg-transparent text-gray-500">
      Auth Layout
    </span>
    <a
      use:link
      href="/auth/login"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Login
    </a>
    <a
      use:link
      href="/auth/register"
      class="text-sm py-2 px-4 font-normal block w-full whitespace-no-wrap bg-transparent text-gray-800">
      Register
    </a>
  </div>
</div>
