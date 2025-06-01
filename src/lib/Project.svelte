<script>
    export let data; //placeholder for data, so that any source can be used
</script>

<article>
    <div class="inner-grid">
        <h2> {data.title} </h2>
        <p> {data.description} </p>
        {#each data.stack as s}
            <p>{s}</p>
        {/each} 
    </div>
    <a href={data.link}><img src={data.image} alt="blank"></a>  
</article>

<style>
    .inner-grid {
        display: grid;
        grid-template-columns: repeat(2, 1fr) max-content;
    }
    
</style>