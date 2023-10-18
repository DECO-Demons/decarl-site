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
            <p class="box">
                Create and upload your own digital masterpieces for others to discover and enjoy!
            </p>
        </span>
        <span class="info-col">
            <div class="box icon-box" id="connect-icon-box">
                <Network size={iconSize} strokeWidth={iconStrokeWidth} color={iconFill} />
            </div>
            <h3>Connect</h3>
            <p class="box">
                Stay up to date on emerging digital art culture by adding friends and following creators!
            </p>
        </span>
        <span class="info-col">
            <div class="box icon-box" id="explore-icon-box">
                <Search size={iconSize} strokeWidth={iconStrokeWidth} color={iconFill} />
            </div>
            <h3>Explore</h3>
            <p class="box">
                Find unique digital artwork, adding new life to the places you're familiar with!
            </p>
        </span>
    </div>
</section>

<style>
    #about-section {
        min-height: 50vh;
        padding-top: 3rem;
    }

    #three-col-info {
        display: flex;
        flex-direction: row;
        width: 75%;
        margin: 0 auto;
        justify-content: space-between;
        align-items: center;
    }

    @media only screen and (max-width: 768px) {
        #three-col-info {
            flex-direction: column;
            justify-content: center;
            align-items: center;
            gap: 5rem;
        }
    }

    .info-col {
        display: flex;
        width: 27ch;
        flex-direction: column;
        gap: 0rem;
        align-items: center;
    }

    .info-col > p {
        text-align: center;
        background-color: var(--grey-050);
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
