<section id="demo">
    <div class="demo-videos">
        <video autoplay muted>
            <source src="/demo-videos/explore.mp4" type="video/mp4">
        </video>
        <video autoplay muted>
            <source src="/demo-videos/C0024.mp4" type="video/mp4">
        </video>
        <video autoplay muted>
            <source src="/demo-videos/C0024_2.mp4" type="video/mp4">
        </video>
    </div>
</section>

<style>
    #demo {
        padding: 4rem 0;
        width: 70%;
        display: flex;
        flex-direction: column;
        margin: 0 auto
    }

    .demo-videos {
        display: flex;
        flex-direction: row;
        justify-content: space-between;
        align-items: center;
    }

    @media only screen and (max-width: 768px) {
        .demo-videos {
            flex-direction: column;
            gap: 5rem;
        }
    }

    #middle-video {
        flex-direction: row-reverse;
    }

    p {
        background: var(--grey-050);
        height: 20rem;
    }
        
    video {
        height: 60vh;
        width: auto;
        border-radius: 30px;
        pointer-events: none;
    }
</style>
