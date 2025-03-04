<script>
    import { onMount } from 'svelte';
    export let events = [];
  
    let currentMonth = new Date().getMonth();
    let currentYear = new Date().getFullYear();
    let daysInMonth = [];
  
    // Function to get the number of days in a month
    function getDaysInMonth(year, month) {
      return new Date(year, month + 1, 0).getDate();
    }
  
    // Function to generate the calendar days
    function generateCalendar(year, month) {
      daysInMonth = [];
      const totalDays = getDaysInMonth(year, month);
      const firstDayOfMonth = new Date(year, month, 1).getDay();
  
      // Add blank cells for days before the first of the month
      for (let i = 0; i < firstDayOfMonth; i++) {
        daysInMonth.push({ date: null });
      }
  
      // Add cells for each day of the month
      for (let day = 1; day <= totalDays; day++) {
        const dateString = new Date(year, month, day).toISOString().split('T')[0];
        const eventsForDay = events.filter(e => new Date(e.date).toISOString().split('T')[0] === dateString);
        daysInMonth.push({ date: day, events: eventsForDay });
      }
    }
  
    // Initialize the calendar
    onMount(() => {
      generateCalendar(currentYear, currentMonth);
    });
  
    // Handle month navigation
    function changeMonth(direction) {
      currentMonth += direction;
      if (currentMonth < 0) {
        currentMonth = 11;
        currentYear--;
      } else if (currentMonth > 11) {
        currentMonth = 0;
        currentYear++;
      }
      generateCalendar(currentYear, currentMonth);
    }
  </script>
  
  <div class="calendar-container mx-auto py-4 px-2 sm:px-4 md:py-8">
    <!-- Month Navigation -->
    <div class="flex justify-between items-center mb-4 sm:mb-6">
      <button on:click={() => changeMonth(-1)} class="px-2 py-1 sm:px-4 sm:py-2 bg-purple-600 text-white rounded hover:bg-purple-700 text-xs sm:text-sm">
        &larr; Prev
      </button>
      <h2 class="text-base sm:text-xl font-bold">
        {new Date(currentYear, currentMonth).toLocaleDateString(undefined, { month: 'long', year: 'numeric' })}
      </h2>
      <button on:click={() => changeMonth(1)} class="px-2 py-1 sm:px-4 sm:py-2 bg-purple-600 text-white rounded hover:bg-purple-700 text-xs sm:text-sm">
        Next &rarr;
      </button>
    </div>
  
    <!-- Calendar Grid -->
    <div class="grid grid-cols-7 gap-1 sm:gap-2 border-t border-l text-center">
      <!-- Weekday Headers -->
      {#each ['S', 'M', 'T', 'W', 'T', 'F', 'S'] as day, i}
        <div class="p-1 sm:p-2 font-semibold border-r border-b bg-gray-200 text-xs sm:text-sm">
          <span class="hidden sm:inline">{['Sun', 'Mon', 'Tue', 'Wed', 'Thu', 'Fri', 'Sat'][i]}</span>
          <span class="sm:hidden">{day}</span>
        </div>
      {/each}
  
      <!-- Calendar Days -->
      {#each daysInMonth as { date, events }}
        <div class="relative p-1 sm:p-2 border-r border-b min-h-[60px] sm:min-h-[80px] md:min-h-[100px] overflow-y-auto">
          {#if date}
            <div class="font-semibold text-xs sm:text-sm">{date}</div>
            {#if events && events.length}
              <div class="flex flex-col gap-1 mt-1">
                {#each events as event, i}
                  {#if i < 2 || window.innerWidth > 640}
                    <div class="text-2xs sm:text-xs bg-purple-200 text-purple-800 rounded px-1 py-0.5 truncate text-left">
                      {event.title}
                    </div>
                  {:else if i === 2}
                    <div class="text-2xs sm:text-xs bg-gray-200 text-gray-800 rounded px-1 py-0.5">
                      +{events.length - 2} more
                    </div>
                  {/if}
                {/each}
              </div>
            {/if}
          {/if}
        </div>
      {/each}
    </div>
  </div>
  
  <style>
    .calendar-container {
      max-width: 100%;
      overflow-x: auto;
    }
    
    @media (min-width: 768px) {
      .calendar-container {
        max-width: 1000px;
      }
    }
    
    /* Ultra small text for tiny events on mobile */
    .text-2xs {
      font-size: 0.65rem;
    }
    
    /* Ensure the calendar doesn't break layout on small screens */
    @media (max-width: 380px) {
      .calendar-container {
        font-size: 0.7rem;
      }
    }
  </style>