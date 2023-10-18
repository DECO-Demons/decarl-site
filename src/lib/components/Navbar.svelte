<script lang="ts">
    import OnMount from "$lib/helpers/OnMount.svelte";
    
</script>

<span id="navbar-container">
    <span id="navbar">
        <span id="nav-items" class="box">
            <OnMount>
                {#each document.querySelectorAll("section") as section}
                    {#if section.id != "hero-section"}
                        <a href={"#" + section.id}>
                            <span class="nav-item">
                                {section.id.split("-")[0].toUpperCase()}
                            </span>
                        </a>
                    {/if}
                {/each}
            </OnMount>
        </span>
    </span>
</span>

<style>
    #navbar-container {
        top: 0;
        width: 100%;
        position: fixed;
    }
    
    #navbar {
        overflow: hidden;
        margin: 0 auto;
        padding: 0.5rem 0;
        display: flex;
        flex-direction: row;
        justify-content: center;
        align-items: center;
        width: 70%;
    }

    #nav-items {
        display: flex;
        flex-direction: row;
        padding: 0.5rem 0;
        background-color: var(--background-1);
    }

    #nav-items a {
        text-decoration: none;
    }

    .nav-item {
        font-weight: bold;
        padding: 0.5rem 1rem;
        user-select: none;
    }

    .nav-item:hover {
        color: var(--background-1);
        background: var(--grey-900);
    }

    a:first-child * {
        border-radius: 7px 0 0 7px;
    }

    a:last-child * {
        border-radius: 0px 7px 7px 0;
    }
</style>
