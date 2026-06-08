<script>
    import pic from '$lib/assets/personal_pic_2.png';
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
        i'm a budding tech policymaker, studying at the UC Berkeley School of Information.  my goal in life is to ensure novel technologies are built in ways that <mark> amplifies the agency and dignity </mark> of people who need it most. 
        </p>
        <p>
        as such, i'm most interested in analyzing the <mark> systemic behavior of emerging ai</mark>, and how they impact one's <mark>civil liberties and human rights.</mark>
        </p>
        <p>    
        i grew up in california and recently graduated from wellesley college in computer science and economics.
        </p>
        <p>
        in my free time, i'll be found reading the New Yorker, baking chocolate chip banana bread, or working out!
        </p>
        <p>
        you can reach me at <strong id='email'>ashima_kamra@berkeley.edu</strong>
        </p>
    </div>
    <!-- need to figure out how to utilize media queries -->
    <img src={pic} alt="photo of me in a library" /> 
</div>

<style>

    mark {
        background-color: var(--accent2);
        color: white;
        font-style: bold;
    }

    #email {
        color: var(--accent3);
    }
    
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
        padding-top: 1em;
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


