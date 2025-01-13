<script>
    import Teaminfo from "./Teaminfo.svelte";
</script>

<main>

    <section class="py-16 mt-20"> 
        <div class="container mx-auto px-6 md:px-10">
            <div class="flex flex-col md:flex-row items-center md:space-x-10 space-y-8 md:space-y-0">
              <!-- Image Section -->
              <div class="text-center md:text-left max-w-lg">
                <h1 class="font-bold text-3xl md:text-4xl leading-tight text-gray-800">
                 Our Mission
                </h1>
                <p class="text-gray-600 mt-4">
                  We empower women to excel and advance in engineering, recognizing their significant 
                  contributions as leaders. SWE at CSUF fosters a supportive community for future 
                  engineers and leaders.
                </p>
               
              </div>
              <div class="flex justify-center">
                <img 
                  class="w-full max-w-sm md:max-w-md rounded-lg shadow-lg" 
                  src="/assets/img-4.webp" 
                  alt="our-mission"
                />
              </div>
              <!-- Text Section -->
             
            </div>
          </div>
    </section>


    <!-- board section  -->

    <section  class=" bg-purple-50 py-16 mt-20"> 
       <Teaminfo />

    </section>

</main>

<style>
     .container {
      max-width: 1200px; /* Adjust for your design */
    }

</style>