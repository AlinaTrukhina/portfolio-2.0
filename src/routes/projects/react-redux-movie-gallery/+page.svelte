<script>
    import reduxmoviesrecording from '$lib/screenCaptures/reduxmoviesscreenrecording.mp4';

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
		if (new Date() - lastMouseDown < 3000) {
			if (paused) e.target.play();
			else e.target.pause();
		}
	}

    const techsUsed = [
    'React',
    'Redux',
    'Redux-Saga',
    'Node.js',
    'PostgreSQL',
    'Material-UI'
    ]
</script>

<svelte:head>
	<title>React-Redux Movie Gallery</title>
	<meta name="description" content="React-Redux Movie Gallery" />
</svelte:head>

<section class="projectReactGallery">
    <h1>React-Redux Movie Gallery</h1> 

    <p>
This project focused on creating a responsive movie gallery website.
    </p>
    <p>
The movie list will be shown on the main page. 
You can click on a movie to go to its details view, and 
the details view will show the movie's genres and description.
    </p>
    <p>
Add a movie to the list using the form. 
Select any number of genres for the film from the drop-down menu.
    </p>

    <div class="screen-capture">
        <h2>Demo</h2>
        <p>Click on video to play</p>
        <video class="recording"
        src={reduxmoviesrecording}
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

    <a href="https://github.com/AlinaTrukhina/weekend-challenge-movie-sagas">
        Source Code on GitHub
    </a>
    
</section>

<style>

</style>