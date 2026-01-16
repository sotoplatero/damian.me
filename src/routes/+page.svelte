<script>
	const projects = [
		{
			name: "freebie.email",
			url: "https://freebie.email",
			logo: "https://freebie.email/favicon-48x48.png",
			description: "Automatiza lead magnets con landing pages y emails",
		},
		{
			name: "article.video",
			url: "https://article.video",
			logo: "https://article.video/logo.png",
			description: "Convierte videos de YouTube en articulos",
		},
		{
			name: "md2.website",
			url: "https://md2.website",
			logo: "https://md2.website/favicon-32x32.png",
			description: "API para publicar Markdown como URLs al instante",
		},
	];
</script>

<svelte:head>
	<title>Damian - Builder</title>
	<meta
		name="description"
		content="Construyo micro SaaS, tools y automatizaciones"
	/>
</svelte:head>

<main class="min-h-screen bg-stone-50 font-sans antialiased">
	<div class="mx-auto max-w-md px-6 py-20">
		<!-- Profile -->
		<header class="flex flex-col items-center text-center">
			<a
				href="https://x.com/sotoplatero"
				target="_blank"
				rel="noopener"
				class="group relative mb-6"
			>
				<img
					src="https://unavatar.io/x/sotoplatero"
					alt="Damian"
					class="h-24 w-24 rounded-full ring-2 ring-stone-200 transition-all duration-300 group-hover:ring-stone-400 group-hover:scale-105"
				/>
			</a>

			<h1 class="text-2xl font-semibold text-stone-900 tracking-tight">
				Damian
			</h1>
			<a
				href="https://x.com/sotoplatero"
				target="_blank"
				rel="noopener"
				class="font-mono text-sm text-stone-500 transition-colors hover:text-stone-900"
			>
				@sotoplatero
			</a>

			<p
				class="mt-4 text-stone-600 leading-relaxed max-w-xs text-sm font-light"
			>
				micro-saas, tools y automatizaciones
			</p>
		</header>

		<!-- Projects -->
		<section class="mt-8">
			<h2
				class="mb-4 font-mono text-xs font-medium uppercase tracking-wider text-stone-400"
			>
				Proyectos
			</h2>
			<ul class="space-y-3">
				{#each projects as project (project.name)}
					<li>
						<a
							href={project.url}
							target="_blank"
							rel="noopener"
							class="group flex items-center gap-3 rounded-xl border border-stone-200 bg-white px-4 py-3 transition-all duration-200 hover:border-stone-300 hover:shadow-sm hover:-translate-y-0.5"
						>
							<img
								src={project.logo}
								alt={project.name}
								class="h-10 w-10 rounded-lg object-contain transition-transform duration-200 group-hover:scale-110"
							/>
							<div class="flex-1 min-w-0">
								<span
									class="font-medium text-stone-900 group-hover:text-black"
								>
									{project.name}
								</span>
								<p
									class="mt-0.5 text-sm text-stone-500 line-clamp-1"
								>
									{project.description}
								</p>
							</div>
							<span
								class="text-stone-300 transition-all duration-200 group-hover:text-stone-500 group-hover:translate-x-0.5"
							>
								→
							</span>
						</a>
					</li>
				{/each}
			</ul>
		</section>
	</div>
</main>
