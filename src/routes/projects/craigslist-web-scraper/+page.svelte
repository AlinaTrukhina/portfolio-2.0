<script>
	import search_results from '$lib/images/search-results.png';
</script>

<svelte:head>
	<title>CLI Tool for Web Scraping Craigslist</title>
	<meta name="description" content="CLI Tool for Craigslist Web Scraping" />
</svelte:head>

<section>
	<h1>CLI Tool for Web Scraping Craigslist</h1>

	<h2 class=website-link>
        <a href="https://www.npmjs.com/package/craigslist-cli-tool" target="_blank" rel="noreferrer">
        NPM Package
        </a>
    </h2>

	<h3>Duration: 4 Day Sprint</h3>

	<p>This is a simple tool for searching Craigslist, designed to be run from the command line. 
		The tool is currently set up to search 'free stuff' section of Minneapolis craigslist for 'dirt',
		 and email the search results to my personal email, every day at 7 am and 1 pm.
    </p>

	<div class="screen-capture">
        <h2>Screenshot</h2>
		<img src={search_results} alt="search results in your email" />
    </div>

    <h3 class=website-link>
        <a href="https://medium.com/@alinatrukhina/creating-a-tool-for-craigslist-web-scraping-a0f092984353" target="_blank" rel="noreferrer">
        Please see my blog for complete writeup
        </a>
    </h3>

	<h2 class="techs-used">Technologies Used</h2>
    <ul>
		<li>JavaScript</li>
        <li>Express</li>
        <li>Selenium Webdriver</li>
        <li>Nodemailer</li>
        <li>node-cron</li>
	</ul>

	<a href="https://github.com/AlinaTrukhina/craigslist-cli-tool">
        Source Code on GitHub
    </a>

</section>

<style>
	.website-link a {
		color: var(--color-theme-2);
		font-size: 0.9em;
	}

	a {
		color: var(--color-theme-pink);
		font-size: 0.9em;
	}
	
	a:hover {
		background-color: var(--color-theme-purple);
		padding: 5px;
		border-radius: 5px;
	}

	.screen-capture {
		display: flex;
		flex-direction: column;
	}

	.techs-used, .screen-capture>h2 {
		margin-bottom: 0;
	}

	img {
		max-width: 400px;
		border-radius: 5px;
	}
	
</style>