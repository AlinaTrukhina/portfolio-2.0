<script>
    import galleryrecording from '$lib/screenCaptures/galleryscreenrecording.mp4';

    // These values are bound to properties of the video
	let paused = true;

	// Used to track time of last mouse down event
	let lastMouseDown;

	// we can't rely on the built-in click event, because it fires
	// after a drag — we have to listen for clicks ourselves
	function handleMousedown(e) {
		lastMouseDown = new Date();
	}

	function handleMouseup(e) {
		if (new Date() - lastMouseDown < 300) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

    const techsUsed = [
    'React',
    'Node.js',
    'PostgreSQL',
    'HTML',
    'CSS',
    'Material UI'
]
</script>

<svelte:head>
	<title>React Photo Gallery</title>
	<meta name="description" content="React Photo Gallery" />
</svelte:head>

<section class="projectReactGallery">
    <h1>React Photo Gallery</h1>    
    
    <h2 class=website-link>
        <a href="https://react-photo-gallery-ant.herokuapp.com/" target="_blank" rel="noreferrer">
        Photo Gallery website
        </a>
    </h2>

    <p>
This app shows photos in a beautiful gallery format, 
where you can click on an image to display it description. 
Clicking the description displays the image.
    </p>
    <p>
You can also like any image by clicking the heart icon, 
or delete it with the trash can icon.
    </p>
    <p>
You can add your own photo to the gallery by entering 
the url and description and clicking submit photo.
    </p>
        
    <div class="screen-capture">
        <h2>Demo</h2>
        <p>Click on video to play</p>
        <video class="recording"
        src={galleryrecording}
		on:mousedown={handleMousedown}
		on:mouseup={handleMouseup}
		bind:paused>
        <track kind="captions">
    </div>
    <h2>Technologies Used</h2>
    <ul>
        {#each techsUsed as tech}
        <li>
            {tech}
        </li>
        {/each}
    </ul>

    <a href="https://github.com/AlinaTrukhina/weekend-react-gallery">
        Source Code on GitHub
    </a>
    
</section>

<style>
.website-link a {
    color: var(--color-theme-pink);
    font-size: 0.9em;
}

.website-link a:hover {
    background-color: var(--color-theme-purple);
    padding: 5px;
    border-radius: 5px;
}

</style>