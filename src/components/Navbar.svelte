<script>
    import { page } from '$app/stores';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
    $: activeUrl = $page.url.pathname;
    let activeClass = 'text-white bg-[#AE93BD] md:bg-transparent md:text-purple-400 md:dark:text-white dark:bg-green-600 md:dark:bg-transparent';
    let nonActiveClass = 'text-gray-700 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-purple-3c00 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent';
  </script>
  
  <Navbar class="border-b-2 ">
    <NavBrand href="/">
      <img src="/assets/logo.png" class="me-3 h-6 sm:h-20" alt="Flowbite Logo" />
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl} {activeClass} {nonActiveClass}>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/about">About</NavLi>
      <NavLi href="/event">Events</NavLi>
      <NavLi href="/join">Join Us</NavLi>
      <!-- <NavLi href="/sponsors">Sponsors</NavLi> -->
      <!-- might get rid of contacts  -->
      <!-- <NavLi href="/docs/components/avatar">Contact</NavLi> -->

    </NavUl>
  </Navbar>