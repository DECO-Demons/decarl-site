<script lang="ts">
    import { onMount } from "svelte";
    
    import { SprayCan, Network, Search } from "lucide-svelte";
    let iconSize = 48;
    let iconStrokeWidth = 2;

    let iconFill = "#000000";
    onMount(() => {
        iconFill = getComputedStyle(document.documentElement).getPropertyValue("--grey-900");
    })
</script>

<section id="about-section">
    <div id="three-col-info">
        <span class="info-col">
            <div class="box icon-box" id="create-icon-box">
                <SprayCan size={iconSize} strokeWidth={iconStrokeWidth} color={iconFill} />
            </div>
            <h3>Create</h3>
        </span>
        <span class="info-col">
            <div class="box icon-box" id="connect-icon-box">
                <Network size={iconSize} strokeWidth={iconStrokeWidth} color={iconFill} />
            </div>
            <h3>Connect</h3>
        </span>
        <span class="info-col">
            <div class="box icon-box" id="explore-icon-box">
                <Search size={iconSize} strokeWidth={iconStrokeWidth} color={iconFill} />
            </div>
            <h3>Explore</h3>
        </span>
    </div>
</section>

<style>
    #about-section {
        min-height: 50vh;
        padding-top: 5rem;
    }

    #three-col-info {
        display: flex;
        flex-direction: row;
        width: 60%;
        margin: 0 auto;
        justify-content: space-between;
    }

    @media only screen and (max-width: 768px) {
        #three-col-info {
            flex-direction: column;
            gap: 5rem;
        }
    }

    .info-col {
        display: flex;
        flex-direction: column;
        gap: 0.5rem;
        align-items: center;
    }

    .icon-box {
        border-radius: 20px;
        padding: 1rem;
    }

    #create-icon-box {
        background: var(--primary-500);
    }
    #connect-icon-box {
        background: var(--secondary-500);
    }
    #explore-icon-box {
        background: var(--tertiary-500);
    }
</style>
