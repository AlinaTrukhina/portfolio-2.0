<script>
    import { page } from '$app/stores';
    import Button from './Button.svelte';

</script>

<section>
    <div class="darkbutton">
        <!-- <Button>
            Toggle light/dark
        </Button> -->
    </div>

    <h1>Alina Trukhina</h1>
    <h2> Full Stack Software Developer</h2>

    <nav class="header-links">
        <ul>
            <li>
                <a class="header-link" href="/">About</a>
            </li>
            <li>|</li>
            <li>
                <a class="header-link" href="/projects">Projects</a>
            </li>
        </ul>
    </nav>
</section>

<style>
:global(body) {
min-height: 100vh;
margin: 0;
background-attachment: fixed;
background-color: var(--color-theme-darkblue);
}

section {
    background-color: var(--color-theme-blue);
}

:global(body.light-mode) {
		background-color: #8bcbff;
		color: #22153c;
}

:global(main.light-mode) {
		background-color: #6db0e7;
		color: #22153c;
}

h1, h2 {
    color: var(--color-theme-pink);
    padding-top: 0.5em;
}

:global(p) {
    color: var(--color-theme-pink);
}

:global(pre) {
    color: var(--color-theme-pink);
}

.darkbutton {
    position: absolute;
    top: 1em;
    right: 0.5em;
}

nav {
    display: flex;
    justify-content: center;
    --background: rgba(255, 255, 255, 0.7);
}

nav a {
    padding: 0.5rem;
    color: var(--color-text);
    font-weight: 700;
    font-size: 1.5rem;
    text-transform: uppercase;
    letter-spacing: 0.1em;
    text-decoration: none;
    transition: color 0.2s linear;
}

a:hover {
    color: var(--color-theme-pink);
    text-decoration: underline;
}

ul {
    list-style: none;
    margin-left: 0;
    padding-left: 0;
}

li {
    display: inline;
    color: var(--color-theme-2);
}

h1 {
    font-size: 2em;
    letter-spacing: 0.1em;
    text-align: center;
}

h2 {
    text-align: center;
}

.header-link {
    padding-top: 0.5em;
}

</style>