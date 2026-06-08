<nav>
    <a href="/" class="logo-link">
        <img src="/logo.svg" alt="logo of colored stars" class="logo">
    </a>
    <a href="/contact">contact</a>
    <a href="https://github.com/ashi-kamra" target="_blank">github</a>
</nav>
<slot />

<style>
    nav {
        display: flex;
        justify-content: center;
        align-items: center;
    }

    .logo-link {
        margin-right: auto;
        display: flex;
    }

    .logo {
        width: 150px;
        height: 150px;
    }

    nav a:not(.logo-link) {
        padding: 1em;
        margin: 1em;
        border: solid 1px var(--accent1);
        border-radius: 5px;
        background-color: var(--accent1);
        text-decoration: none;
        color: white;
    }

</style>
