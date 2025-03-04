<script>
    import { newevents } from "$lib/newevents"; 
    import EventCard from './EventCard.svelte';
</script>

<main>
    <section class="py-16 mt-20 bg-purple-50">
        <div class="container mx-auto px-6 md:px-10">
            <h1 class="font-bold text-3xl md:text-4xl leading-tight text-gray-800 mb-3">
                Upcoming Events: Spring 2025
            </h1>
            
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-3 gap-4">
                {#each newevents as event}
                    <EventCard 
                        title={event.title}
                        date={event.date}
                        image={event.image}
                        link={event.link}
                    />
                {/each}
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