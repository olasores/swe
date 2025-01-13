<script>
	import { P } from "flowbite-svelte";
  
</script>

<main>
    <!-- Hero Section -->
    <section class="bg-gray-100 py-12 flex items-center min-h-screen mb-20">
      <div class="container mx-auto px-4 md:px-6">
        <div class="flex flex-col md:flex-row items-center md:space-x-10 space-y-8 md:space-y-0">
          <!-- Text Section -->
          <div class="text-center md:text-left max-w-2xl">
            <h1 class="font-bold text-4xl md:text-5xl leading-tight">
              <span>Society of</span> <br />
              <span>Women Engineers</span>
            </h1>
            <h2 class="text-lg md:text-xl text-gray-700 mt-4">
              California State University, Fullerton
            </h2>
            <p class="text-gray-600 mt-4">
              Join SWE at CSUF and become part of a supportive community that empowers
              women in engineering with opportunities for growth and success!
            </p>
            <!-- Buttons -->
            <div class="mt-6 flex flex-wrap justify-center md:justify-start gap-4">
              <button class="bg-[#AE93BD] text-white px-6 py-2 rounded-lg hover:bg-[#9554BA] ">
                Join Us
              </button>
              <button class="border-2 border-black px-6 py-2 rounded-lg hover:bg-gray-300">
                Sponsor Us
              </button>
            </div>
          </div>
          <!-- Image Section -->
          <div class="flex justify-center">
            <img
              src="/assets/img-3.webp"
              alt="board-img"
              class="w-full max-w-md md:max-w-lg rounded-lg shadow-lg"
            />
          </div>
        </div>
      </div>
    </section>
  
    <!-- About Section -->
    <section class="py-16 mt-20">
      <div class="container mx-auto px-6 md:px-10">
        <div class="flex flex-col md:flex-row items-center md:space-x-10 space-y-8 md:space-y-0">
          <!-- Image Section -->
          <div class="flex justify-center">
            <img 
              class="w-full max-w-sm md:max-w-md rounded-lg shadow-lg" 
              src="/assets/img-2.webp" 
              alt="Abt-img"
            />
          </div>
          <!-- Text Section -->
          <div class="text-center md:text-left max-w-lg">
            <h1 class="font-bold text-3xl md:text-4xl leading-tight text-gray-800">
              About Us
            </h1>
            <p class="text-gray-600 mt-4">
              We empower women to excel and advance in engineering, recognizing their significant 
              contributions as leaders. SWE at CSUF fosters a supportive community for future 
              engineers and leaders.
            </p>
            <!-- Button -->
            <div class="mt-6">
              
              <a href="/about" class="bg-[#AE93BD] text-white px-6 py-2 rounded-lg shadow hover:bg-[#9554BA] transition-colors">
                Learn More
              </a>
              
            </div>
          </div>
        </div>
      </div>
    </section>

    <!-- Upcoming Events Section -->
    <section class="py-16 mt-20  bg-purple-50">
        <div class="container mx-auto px-6 md:px-10">
        <h1 class="font-bold text-3xl md:text-4xl leading-tight text-gray-800 mb-3 ">
            Upcoming Events: Spring 2025
        </h1>
        
        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4 ">

            <div class="max-w-sm  dark:bg-gray-800 dark:border-gray-700">
                <a href="/">
                    <img class="rounded-t-lg mb-2" src="/assets/game.png" alt="" />
                </a>
                <div class="">
                    <a href="/">
                        <h5 class="mb-0 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Game Night</h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">December 12, 2024</p>
                </div>
            </div>

            <div class="max-w-sm ">
                <a href="/">
                    <img class="rounded-t-lg mb-2" src="/assets/lockpicking.png" alt="" />
                </a>
                <div class="">
                    <a href="/">
                        <h5 class="mb-0 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">Lock Picking</h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">August 13, 2024</p>
                    <!-- <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                        Read more
                        <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                        </svg>
                    </a> -->
                </div>
            </div>

            <div class="max-w-sm ">
                <a href="/">
                    <img class="rounded-t-lg mb-2" src="/assets/painting.png" alt="" />
                </a>
                <div class="">
                    <a href="/">
                        <h5 class="mb-0 text-2xl font-bold tracking-tight text-gray-900 ">Painting</h5>
                    </a>
                    <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">September 12,2024</p>
                    <!-- <a href="#" class="inline-flex items-center px-3 py-2 text-sm font-medium text-center text-white bg-blue-700 rounded-lg hover:bg-blue-800 focus:ring-4 focus:outline-none focus:ring-blue-300 dark:bg-blue-600 dark:hover:bg-blue-700 dark:focus:ring-blue-800">
                        Read more
                        <svg class="rtl:rotate-180 w-3.5 h-3.5 ms-2" aria-hidden="true" xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 14 10">
                            <path stroke="currentColor" stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M1 5h12m0 0L9 1m4 4L9 9"/>
                        </svg>
                    </a> -->
                </div>
        </div>


  



    
        <!-- View All Events Button -->
        <div class="mt-2 text-left">
          <a href="/event" class="bg-[#AE93BD] text-white px-6 py-2 rounded-lg shadow hover:bg-[#9554BA] transition-colors">
            View All Events
          </a>
        </div>
    </div>
    </section>

    
    
    


  </main>
  
  <style>
    /* Centered and consistent padding for all sections */
    .container {
      max-width: 1200px; /* Adjust for your design */
    }
  </style>
  