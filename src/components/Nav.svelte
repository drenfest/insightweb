<script>
	export let segment;
	let routes = [
		{
			slug:'search-engine-optimization',
			text:'Seo',
			title:'Learn About Our Search Engine Optimization Services'
		},
		{
			slug:'social-media-marketing',
			text:'Social Media Marketing',
			title:'Get Your Leads From Our Social Media Marketing Services'
		},
		{
			slug:'website/design',
			text:'Web Design',
			title:'See Our Web Design Services'
		},
		{
			slug:'website/development',
			text:'Web Development',
			title:'See Our Web Development Services'
		},
		{
			slug:'website/hosting',
			text:'Web Hosting',
			title:'Affordable Website Hosting Tailored To Fit Your Needs'
		},
		{
			slug:'portfolio',
			text:'Portfolio',
			title:'View Insight Marketing Solutions Portfolio'
		},
	]
</script>

<style>
	nav {
		border-bottom: 1px solid rgba(255,62,0,0.1);
		font-weight: 300;
		padding: 0 1em;
	}

	ul {
		margin: 0;
		padding: 0;
	}

	/* clearfix */
	ul::after {
		content: '';
		display: block;
		clear: both;
	}

	li {
		display: block;
		float: left;
	}

	.selected {
		position: relative;
		display: inline-block;
	}

	.selected::after {
		position: absolute;
		content: '';
		width: calc(100% - 1em);
		height: 2px;
		background-color: rgb(255,62,0);
		display: block;
		bottom: -1px;
	}

	a {
		text-decoration: none;
		padding: 1em 0.5em;
		display: block;
	}
</style>

<nav>
	<ul>
		<li><a class:selected='{segment === undefined}' title="Go Back To The Homepage" href='.'>Home</a></li>
		{#each routes as route}
			<li><a class:selected='{segment === route.slug}' title="{route.title}" href='{route.slug}'>{route.text}</a></li>
		{/each}
	</ul>
</nav>
