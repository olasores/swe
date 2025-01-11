<script>
    import { pastevents } from "$lib/pastevents";

</script>

<main>
    <!-- Upcoming Events Section -->
  <section class="py-16 mt-20">
    <div class="flex flex-col items-center text-center space-y-6">
      <h1 class="font-extrabold text-3xl md:text-5xl leading-tight text-gray-800">
        Upcoming Events: Spring 2025
      </h1>
      <p class="text-lg text-gray-600">Weekly Meetings: Wednesday at 2:00 PM in ECS 200</p>
      <img class="w-full max-w-3xl rounded-lg shadow-lg" src="/assets/aboutimg.png" alt="Upcoming Events Image" />
    </div>
  </section>



    <section class=" flex flex-col items-center justify-center mt-20  bg-purple-50">
        <div class="text-center mb-10">
            <h1 class="font-extrabold text-3xl md:text-4xl  leading-tight text-gray-800">
              Past Events
            </h1>
            <p class="text-lg text-gray-600 max-w-2xl mx-auto">
              Discover the exciting and impactful events hosted by SWE CSUF! Our past events showcase our commitment to empower.
            </p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 px-4">
            {#each pastevents as event}
            <div class="mb-10 rounded-lg shawdow-d overflow-hidden">
                <a href="/">
                    <img src={event.image} alt={event.title}/>
                </a>
                <div class="mt-2">
                    <a href="/">
                      <h5 class="mb-2 text-2xl font-bold text-gray-800">{event.title}</h5>
                    </a>
                    <p class="text-gray-600">{event.date}</p>
                  </div>
            </div>
            

            {/each}
        </div>

    </section>

</main>

<style>

</style>