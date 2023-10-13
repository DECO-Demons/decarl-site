<script lang="ts">
    import FakeLoadingBar from "$lib/components/FakeLoadingBar.svelte";
    export let splashTime;
</script>

<div class="absolute-center">
    <img
        src="/decarl-logo.png"
        alt="splash-logo"
        id="splash-logo"
    />
    <FakeLoadingBar loadingTime={splashTime} />
</div>

<style>
    .absolute-center {
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        text-align: center;
        height: 101vh;
    }

    #splash-logo {
        max-height: 20rem;
    }
</style>
