<script>
    import { teams } from "$lib/teams";
  </script>
  
  <main class=" bg-purple-50 py-10">
    <div class="container mx-auto px-4">
      <h1 class="text-center text-2xl font-bold text-gray-800 mb-10">Meet Our Team</h1>
      <div class="grid gap-8 sm:grid-cols-2 md:grid-cols-3 lg:grid-cols-4">
        {#each teams as team}
          <div class="align-center text-center p-6 transition-transform transform hover:scale-105">
            <div class="w-40 h-40 mx-auto rounded-full overflow-hidden border-4 border-[#89529f]">
              <img 
                src={team.image || '/default-profile.png'} 
                alt={team.name} 
                class="w-full h-full object-cover"
              />
            </div>
            <h2 class="mt-4 text-lg font-semibold text-gray-700">{team.name}</h2>
            <p class="text-gray-500">{team.role}</p>
          </div>
        {/each}
      </div>
    </div>
  </main>
  