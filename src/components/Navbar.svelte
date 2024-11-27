<script>
    import { page } from '$app/stores';
    import { Navbar, NavBrand, NavLi, NavUl, NavHamburger } from 'flowbite-svelte';
    $: activeUrl = $page.url.pathname;
    let activeClass = 'text-white bg-green-700 md:bg-transparent md:text-green-700 md:dark:text-white dark:bg-green-600 md:dark:bg-transparent';
    let nonActiveClass = 'text-gray-700 hover:bg-gray-100 md:hover:bg-transparent md:border-0 md:hover:text-green-700 dark:text-gray-400 md:dark:hover:text-white dark:hover:bg-gray-700 dark:hover:text-white md:dark:hover:bg-transparent';
  </script>
  
  <Navbar class="border-b-2">
    <NavBrand href="/">
      <img src="/assets/logo.png" class="me-3 h-6 sm:h-20" alt="Flowbite Logo" />
    </NavBrand>
    <NavHamburger />
    <NavUl {activeUrl} {activeClass} {nonActiveClass}>
      <NavLi href="/">Home</NavLi>
      <NavLi href="/docs/components/navbar">About</NavLi>
      <NavLi href="/docs/components/accordion">Events</NavLi>
      <NavLi href="/docs/components/alert">Join Us</NavLi>
      <NavLi href="/docs/components/avatar">Sponsors</NavLi>
      <!-- might get rid of contacts  -->
      <NavLi href="/docs/components/avatar">Contact</NavLi>

    </NavUl>
  </Navbar>