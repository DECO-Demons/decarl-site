<script>
    import OnMount from "$lib/helpers/OnMount.svelte";
    import { fade, fly, scale } from "svelte/transition";
    
    import Splash from "$lib/sections/Splash.svelte";
    import About from "$lib/sections/About.svelte";
    import Demo from "$lib/sections/Demo.svelte";

    import FakeLoadingBar from "$lib/components/FakeLoadingBar.svelte";

    const transitionTime = 600;
    const splashTime = 2500;
    const totalSplashTime = transitionTime + splashTime;

    let splashActive = true;
    setTimeout(() => {splashActive = false}, splashTime);

    let splashFinished = false;
    setTimeout(() => {splashFinished = true}, totalSplashTime);
</script>

{#if splashActive}
    <div out:fade={{ duration: transitionTime }}>
        <OnMount>
            <div in:fade={{ duration: transitionTime }}>
                <Splash {splashTime} />
            </div>
        </OnMount>
    </div>
{:else if splashFinished}
    <div in:scale={{ duration: 300 }}>
        <About />
        <Demo />
    </div>
{/if}
