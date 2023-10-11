<script>
    import { afterNavigate, beforeNavigate } from "$app/navigation";
    import { tweened } from "svelte/motion";
    import { cubicInOut } from "svelte/easing";
    
    let showLoadingBar = true;
    export let loadingTime;
    
    const progress = tweened(0, {
        duration: loadingTime, // The time it takes to move between values
        easing: cubicInOut, // The easing function to use
    });

    progress.set(0);
    progress.set(1);
</script>

{#if showLoadingBar}
    <div class="progress-bar">
        <div class="progress-sliver" style="width: {$progress * 100}%" />
    </div>
{/if}

<style>
    .progress-bar {
         width: 20rem;
         height: 1rem;
         background: var(--grey-200);
         outline: 3px dashed var(--grey-800);
         border-radius: 200px;
     }
    
     .progress-sliver {
         background: var(--primary-500);
         height: 100%;
         border-radius: 200px;
     }
</style>
