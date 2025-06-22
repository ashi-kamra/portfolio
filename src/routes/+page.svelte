<script>
    import pic from '$lib/assets/portfolio-pic.jpeg';
    let text = "hi! i'm ashi.  ";
    let marquee= Array(15).fill(text);
</script>

<div class="marquee">
    <div class="marquee-content">
        <div class="marquee-text">
            {#each marquee as text}
                <h1>{text} &nbsp</h1>
            {/each}
        </div>
        <div class="marquee-text">
            {#each marquee as text}
                <h1>{text} &nbsp</h1>
            {/each}
        </div>
    </div>
</div>

<div id="personal-description">
    <div id="inner-grid">
        <p>
        i'm a budding civic technologist, studying computer science and economics at Wellesley College. i believe the best things are made when they are crafted with intention, care, and with the complexity of the human experience in mind. 
        </p>
        <p>    
            my goal in life is to build technology that amplifies the agency of people who need it most. 
        </p>
    </div>
    <!-- need to figure out how to utilize media queries -->
    <img src={pic} alt="photo of me holding a flower" /> 
</div>

<style>
    
    .marquee {
        overflow: hidden;
        width: 100vw;
    }

    .marquee-content {
        display: flex;
        animation: scroll 35s linear infinite;
        width: max-content;
    }

    /* If using Option 2, add this: */
    .marquee-text {
        display: flex;
    }

    .marquee-text h1 {
        padding-left: 1;

    }

@keyframes scroll {
    from {
        transform: translateX(0);
    }
    to {
        transform: translateX(-50%); /* Move by half the total width */
    }
}

    #personal-description {
        display: flex;
        justify-content: space-evenly;
    }

    #inner-grid {
        width: 40vw;
    }

    img {
        height: auto;
        width: 30vw;
    }

    @media screen and (max-width: 900px) { 
        /* NEED TO ADJUST */
        #personal-description {
            display: flex;
            flex-direction: column;
            align-items: center;
        }

        #inner-grid {
            margin: 2em;
            width: auto;
        }

        img {
            padding-top: 2em;
            width: 50%;
            align-self: center;
        }
    }

</style>


