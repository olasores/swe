<script>
    export let title;
    export let date;
    export let image;
    export let link; 
</script>

<div class="max-w-sm transition-transform transform hover:scale-105">
    <a href={link}>
        <img class="rounded-lg mb-2" src={image} alt={title} />
    </a>
    <div class="">
        <a href={link}>
            <h5 class="mb-0 text-2xl font-bold tracking-tight text-gray-900 dark:text-white">{title}</h5>
        </a>
        <p class="mb-3 font-normal text-gray-700 dark:text-gray-400">{date}</p>
    </div>
</div>
