<script lang="ts">
    // Do a smooth scroll thing
</script>

<span id="navbar-container">
    <span id="navbar">
        <span id="nav-items" class="box">
            <a href="#about-section">
                <span class="nav-item">
                    ABOUT
                </span>
            </a>
            <a href="#demo-section">
                <span class="nav-item">
                    DEMO
                </span>
            </a>
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
        background-color: var(--secondary-200);
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
        color: var(--tertiary-100);
        background: var(--grey-900);
    }

    a:first-child * {
        border-radius: 7px 0 0 7px;
    }

    a:last-child * {
        border-radius: 0px 7px 7px 0;
    }
</style>
