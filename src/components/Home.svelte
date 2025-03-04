<script>
	import { P } from "flowbite-svelte";
  import Events2025 from "./Events2025.svelte";
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
     <section class="">
        <Events2025 />
        
     </section>
  
    
    
    


  </main>
  
  <style>
    /* Centered and consistent padding for all sections */
    .container {
      max-width: 1200px; /* Adjust for your design */
    }
  </style>
  