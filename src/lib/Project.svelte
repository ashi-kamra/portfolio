<script>
    export let data; //placeholder for data, so that any source can be used
</script>

<article>
    <div class="outer-grid">
        <h2> {data.title} </h2>
        <p> {data.description} </p>
        <div class="inner-grid">
            {#each data.stack as s}
                <p>{s}</p>
            {/each} 
        </div>
    </div>
    <a href={data.link}><img src={data.image} alt="blank"></a>  
</article>

<style>
    .inner-grid {
        display: grid;
        grid-template-columns: repeat(3, 100px);
    }

    article {
        display: grid;
        grid-template-columns: repeat(3, 1fr);
    }
    
    img {
        width: 50%;
        height: 75%;
    }
    
</style>