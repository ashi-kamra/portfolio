<script>
    import pic from '$lib/assets/portfolio-pic.jpeg';
    let text = "hi! i'm ashi. ";
    let marquee= Array(10).fill(text);
</script>

<div class="marquee">
    <div class="marquee-content">
         {#each marquee as text}
            <h1>{text}</h1>
        {/each}
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
    <picture>
        <!-- need to figure out how to utilize media queries -->
        <img src={pic} alt="photo of me holding a flower" />

    </picture> 
</div>

<style>
    
    .marquee-content {
        animation: scroll 10s linear infinite;
    }

    #personal-description {
        display: flex;
        justify-content: space-evenly;
    }

    #inner-grid {
        width: 35vw;
    }

    img {
        height: 60vh;
        width: 26vw;
    }

     @keyframes scroll {
        from {
            transform: translateX(100%);
        }
        to {
            transform: translateX(-100%);
        }
    }

</style>


