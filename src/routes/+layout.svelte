<nav>
    <a href="/" class="logo-link">
        <img src="/logo.svg" alt="logo of colored stars" class="logo">
    </a>
    <a href="https://docs.google.com/document/d/1rMh7Jf68BE3TJftG9W7Ie0ACV_0Y2mBAtfRQaXiBMO8/edit?usp=sharing">resume</a>
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
