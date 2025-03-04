<script>
    import { pastevents } from "$lib/pastevents"; 
	import { tick } from "svelte";
    import EventCalendar from "./EventCalendar.svelte";

    export const springevents = [
    { title: 'DiscoverFest', date: 'Jan 29, 2025', image: 'assets/dfest.webp' },
    { title: 'Welcome Back Event', date: 'Feb 12, 2025', image: 'assets/buzz.jpg' },
    { title: 'Titan Rover X SWE: Arduino Workshop ', date: 'Feb 25, 2025', image: 'assets/lin.jpg' },
    { title: 'Robotics Project Meeting', date: 'Feb 26, 2025', image: 'assets/lin.jpg' },
    { title: 'Photo Card Decoration', date: 'March 5, 2025', image: 'assets/lin.jpg' },
    { title: 'Soaring to Success:', date: 'March 7, 2025', image: 'assets/lin.jpg' },
    {title: 'Project Meeting with Jasmine', date: 'March 12, 2025', image: 'assets/lin.jpg'},
    { title: 'Code & Crush Hackathon', date: 'March 14, 2025', image: 'assets/cardf.jpeg' },
    { title: 'Women in Tech Speaker Panel Collab with WIBS', date: 'March 19, 2025', image: 'assets/img-6.webp' },
    { title: 'Project Session', date: 'March 26, 2025', image: 'assets/lp.jpg' },
    { title: 'WIBS 3D Printing Workshop Collab with WIBS', date: 'March 27, 2025', image: 'assets/lin.jpg' },
    { title: 'Test Engineer Talk with Angie)', date: 'April 16, 2025', image: 'assets/lin.jpg' },
    { title: 'Bonfire Potluck End of Year Celebration', date: 'April 28, 2025', image: 'assets/lin.jpg' }
  ];


</script>

<main>
    <!-- Upcoming Events Section -->
  <section class="py-16 mt-20">
    <div class="flex flex-col items-center text-center space-y-6">
      <h1 class="font-extrabold text-3xl md:text-5xl leading-tight text-gray-800">
        Upcoming Events: Spring 2025
      </h1>
      <p class="text-lg text-gray-600">Weekly Meetings: Wednesday at 2:00 PM in ECS 200</p>
      <img class="w-full max-w-3xl rounded-lg shadow-lg" src="/assets/img-5.webp" alt="Upcoming-img" />
      <h1 class="font-bold text-2xl md:text-3xl p-4">Event Calendar</h1>

    </div>
    <EventCalendar events={springevents} />
  </section>




    <section class=" flex flex-col items-center justify-center mt-20  bg-purple-50">
        <div class="text-center mb-10">
            <h1 class="mt-5 font-extrabold text-3xl md:text-4xl  leading-tight text-gray-800">
              Past Events
            </h1>
            <p class="text-lg text-gray-600 max-w-2xl mx-auto">
              Discover the exciting and impactful events hosted by SWE CSUF! Our past events showcase our commitment to empower.
            </p>
        </div>

        <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-8 px-4">
            {#each pastevents as event}
            <div class="mb-10 shawdow-d overflow-hidden transition-transform transform hover:scale-105">
                <a href="/">
                    <img class="rounded-lg"  src={event.image} alt={event.title}/>
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