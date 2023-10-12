<script lang="ts">
    import { SprayCan, Network, Search } from "lucide-svelte";
    let iconSize = 48;
    let iconStrokeWidth = 2;
</script>

<section id="about-section">
    <div id="three-col-info">
        <span class="info-col">
            <SprayCan size={iconSize} strokeWidth={iconStrokeWidth} />
            <h3>Create</h3>
        </span>
        <span class="info-col">
            <Network size={iconSize} strokeWidth={iconStrokeWidth} />
            <h3>Connect</h3>
        </span>
        <span class="info-col">
            <Search size={iconSize} strokeWidth={iconStrokeWidth} />
            <h3>Explore</h3>
        </span>
    </div>
</section>

<style>
    #about-section {
        height: 50vh;
        padding-top: 5rem;
        background: var(--secondary-100);
    }

    #three-col-info {
        display: flex;
        flex-direction: row;
        width: 60%;
        margin: 0 auto;
        justify-content: space-between;
    }

    .info-col {
        display: flex;
        flex-direction: column;
        gap: 2rem;
        align-items: center;
    }
</style>
