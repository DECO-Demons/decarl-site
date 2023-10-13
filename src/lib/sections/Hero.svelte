<section id="hero-section">
    <div id="tagline-container">
        <img
            src="/decarl-logo.png"
            alt="tagline-logo"
            id="tagline-logo"
        />
        <h3 id="tagline-text" class="box">A new age of digital art</h3>
    </div>
    <div id="hero-arts">
        <img
            src="/art-world-paint.png"
            alt="hero-art-painting"
            class="hero-art"
        />
        <img
            src="/art-texting.png"
            alt="hero-art-texting"
            class="hero-art"
        />
        <img
            src="/art-hanging-frame.png"
            alt="hero-art-hanging-frame"
            class="hero-art"
        />
    </div>
</section>

<style>
    #hero-section {
        display: flex;
        padding-top: 7rem;
        flex-direction: column;
        height: 100vh;
    }

    #tagline-container {
        margin: 0 auto;
    }

    #tagline-logo {
        margin: 0 auto;
        display: flex;
        height: 5rem;
    }

    #tagline-text {
        background-color: var(--grey-050);
        padding: 1.5rem;
        margin-top: -1.5rem;
    }

    #hero-arts {
        height: 100%;
        display: flex;
        flex-direction: row;
        align-items: center;
        margin: 0 auto;
        gap: 10rem;
    }

    .hero-art {
        height: 15rem;
    }
</style>
