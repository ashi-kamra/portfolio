
<nav>
    <a href="/projects">projects</a>
    <a href="/other">other</a>
    <a href="/contact">contact</a>
    <a href="https://github.com/ashi-kamra" target="_blank">github</a>
</nav>
<slot />

<style>
    nav {
        display: flex;
        justify-content: center;
        
    }

    nav a {
        padding: 1em;
        margin: 1em;
        border: solid 1px var(--accent1);
        border-radius: 5px;
        background-color: var(--accent1);
        text-decoration: none;
        color: white;
    }

</style>
