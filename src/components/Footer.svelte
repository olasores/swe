<script>
  import { Footer } from 'flowbite-svelte';
  import { InstagramSolid, DiscordSolid, FacebookSolid, MailBoxSolid } from 'flowbite-svelte-icons';
</script>

<Footer class=" text-white py-8 bg-[#AE93BD]">
  <div class="container mx-auto flex flex-col md:flex-row justify-between items-center">
    <!-- Left Section: SWE Info -->
    <div class="text-center md:text-left">
      <h3 class="text-lg font-semibold">SWE @ CSUF 2025</h3>
      <!-- <p class="text-sm mt-1">Aspiring Software Engineer with a passion for web development and data science.</p> -->
    </div>

    <!-- Right Section: Contact and Social Links -->
    <div class="mt-4 md:mt-0 flex space-x-6">
      <!-- Instagram -->
      <a href="https://www.instagram.com/csufswe/?hl=en" target="_blank" class="hover:text-gray-400">
        <InstagramSolid class="w-6 h-6" />
      </a>

      <!-- Discord -->
      <a href="https://discord.gg/NJ3pPnPk" target="_blank" class="hover:text-gray-400">
        <DiscordSolid class="w-6 h-6" />
      </a>

      <!-- <a href="https://facebook.com" target="_blank" class="hover:text-gray-400">
        <FacebookSolid class="w-6 h-6" />
      </a> -->

      <!-- Email -->
      <a href="mailto:swecsuf.president@gmail.com" class="hover:text-gray-400">
        <MailBoxSolid class="w-6 h-6" />
      </a>
    </div>
  </div>
</Footer>
