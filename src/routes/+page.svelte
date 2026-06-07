<script lang="ts">
	type Tool = {
		name: string;
		domain: string;
		url?: string;
		category: string;
		status: 'Live' | 'Coming soon';
		job: string;
	};

	const tools: Tool[] = [
		{
			name: 'FussyFix',
			domain: 'fussyfix.co.uk',
			url: 'https://fussyfix.co.uk',
			category: 'Family & care',
			status: 'Live',
			job: 'A calm planning helper for fussy eating, family meals, and the small negotiations around the table.'
		},
		{
			name: 'PetCompass',
			domain: 'petcompass.uk',
			url: 'https://petcompass.uk',
			category: 'Everyday',
			status: 'Live',
			job: 'A quick decision tool for everyday pet questions, from breeds and routines to the next sensible step.'
		},
		{
			name: 'FlowersFor',
			domain: 'flowersfor.co.uk',
			url: 'https://flowersfor.co.uk',
			category: 'Occasions',
			status: 'Live',
			job: 'A plain-speaking flower chooser for birthdays, sympathy, apologies, thanks, and moments that need handled properly.'
		},
		{
			name: 'LocalAdReckoner',
			domain: 'local-ad-reckoner',
			url: 'https://local-ad-reckoner.netlify.app',
			category: 'Small business',
			status: 'Live',
			job: 'A quick reckoner for deciding whether local advertising spend has a fighting chance of paying its way.'
		},
		{
			name: 'WriteUnblock',
			domain: 'writeunblock.co.uk',
			url: 'https://writeunblock.co.uk',
			category: 'Writing',
			status: 'Live',
			job: 'A simple writing unblocker for getting from a stuck page to a usable next sentence.'
		},
		{
			name: 'PujaCompass',
			domain: 'puja-compass-preview',
			url: 'https://puja-compass-preview.netlify.app',
			category: 'Occasions',
			status: 'Live',
			job: 'A respectful occasion guide for planning puja moments, timings, and practical preparation.'
		},
		{
			name: 'LandlordReadyRenter',
			domain: 'landlord-ready-renter',
			url: 'https://landlord-ready-renter.netlify.app',
			category: 'Home & money',
			status: 'Live',
			job: 'A renter-readiness checklist for turning a property application into something less hopeful and more prepared.'
		},
		{
			name: 'Broadband Switch Calculator',
			domain: 'switchready.co.uk',
			category: 'Home & money',
			status: 'Coming soon',
			job: 'A broadband switching calculator for working out whether the saving is worth the faff before you start.'
		}
	];

	const categories = ['Family & care', 'Everyday', 'Occasions', 'Small business', 'Writing', 'Home & money'];
</script>

<svelte:head>
	<title>Naeproblem — Small tools for everyday decisions</title>
	<meta
		name="description"
		content="Naeproblem is a collection of independent practical tools that help people make everyday decisions — from pets and meal planning to renting, writing, and local business."
	/>
	<meta property="og:title" content="Naeproblem — Small tools for everyday decisions" />
	<meta
		property="og:description"
		content="Independent practical tools for everyday decisions. No accounts. No dashboards."
	/>
	<meta property="og:type" content="website" />
</svelte:head>

<main class="site-shell">
	<section class="hero" aria-labelledby="page-title">
		<p class="eyebrow">Independent practical tools</p>
		<h1 id="page-title">Naeproblem</h1>
		<p class="tagline">Small tools for everyday decisions.</p>
		<p class="descriptor">
			Naeproblem is a collection of independent practical tools that help people make everyday
			decisions — from pets and meal planning to renting, writing, and local business.
		</p>
		<p class="subline">No accounts. No dashboards. Just useful answers, one problem at a time.</p>
	</section>

	<section class="directory" aria-labelledby="tools-title">
		<div class="section-heading">
			<p class="eyebrow">The tools</p>
			<h2 id="tools-title">Browse the tools.</h2>
			<p>Pick a practical helper for food, pets, writing, renting, flowers, and small business decisions.</p>
		</div>

		<div class="category-strip" aria-label="Tool categories">
			{#each categories as category}
				<span>{category}</span>
			{/each}
		</div>

		<div class="tool-grid">
			{#each tools as tool}
				<article class:coming-soon={tool.status === 'Coming soon'} class="tool-card">
					<div class="card-topline">
						<span class="badge">{tool.category}</span>
						<span class="status">{tool.status}</span>
					</div>
					<h3>{tool.name}</h3>
					<p>{tool.job}</p>
					<div class="card-footer">
						{#if tool.url}
							<a href={tool.url} rel="noopener noreferrer">Open tool</a>
						{:else}
							<span class="soon-label">Coming soon</span>
						{/if}
					</div>
				</article>
			{/each}
		</div>
	</section>
</main>

<footer>
	<p>Independent tools. Not an official government or council service.</p>
	<p>Some related civic, cultural, and sport projects are maintained separately.</p>
	<p>No affiliate links on this page.</p>
</footer>
