<script>
    import OnMount from "$lib/helpers/OnMount.svelte";
    import { fade, fly, scale } from "svelte/transition";

    import Navbar from "$lib/components/Navbar.svelte";
    
    import Splash from "$lib/sections/Splash.svelte";
    import Hero from "$lib/sections/Hero.svelte";
    import About from "$lib/sections/About.svelte";
    import Demo from "$lib/sections/Demo.svelte";

    import FakeLoadingBar from "$lib/components/FakeLoadingBar.svelte";

    const splashInTime = 600;
    const splashOutTime = 200;
    const splashTime = 2500;
    const totalSplashTime = splashTime + splashOutTime;

    let splashActive = true;
    setTimeout(() => {splashActive = false}, splashTime);

    let splashFinished = false;
    setTimeout(() => {splashFinished = true}, totalSplashTime);
</script>

{#if splashActive}
    <div out:scale={{ duration: splashOutTime }}>
        <OnMount>
            <div in:fade={{ duration: splashInTime }}>
                <Splash {splashTime} />
            </div>
        </OnMount>
    </div>
{:else if splashFinished}
    <div in:fade={{ duration: 300 }}>
        <Navbar />
        <Hero />
        <Demo />
        <About />
    </div>
{/if}
