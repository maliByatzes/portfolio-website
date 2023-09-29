<script lang="ts">
	import '../app.postcss';
	import logo from "$lib/images/logo-no-background.png"
	import ghLogo from "$lib/images/github-mark.png"
	import { Button } from '$lib/components/ui/button';
	import * as Sheet from "$lib/components/ui/sheet";
</script>

<header class="w-full h-16 flex items-center border-b-2 border-slate-200">
	<nav class="w-full flex items-center justify-between px-5 lg:px-20 sticky">
		<div class="lg:hidden">
			<Sheet.Root>
				<Sheet.Trigger>
					<svg xmlns="http://www.w3.org/2000/svg" fill="none" viewBox="0 0 24 24" stroke-width="1.5" stroke="currentColor" class="w-6 h-6">
						<path stroke-linecap="round" stroke-linejoin="round" d="M11.25 4.5l7.5 7.5-7.5 7.5m-6-15l7.5 7.5-7.5 7.5" />
					</svg>					
				</Sheet.Trigger>
				<Sheet.Content side="left">
					<Sheet.Header>
						<Sheet.Title class="border-b-2 border-slate-200 py-4">
							<a href="/">
								<img src={logo} alt="MZ logo" width="40">
							</a>
						</Sheet.Title>
					</Sheet.Header>
					<div class="flex flex-col gap-4 justify-center w-full">
						<a href="/about-me">
							<Button variant="ghost" class="w-full my-2">About Me</Button>
						</a>
			
						<a href="/skills">
							<Button variant="ghost" class="w-full my-2">My Skills</Button>
						</a>
			
						<a href="/projects">
							<Button variant="ghost" class="w-full my-2">Projects</Button>
						</a>

						<a href="/contact">
							<Button variant="ghost" class="w-full my-2">Contact</Button>
						</a>
					</div>
				</Sheet.Content>
			</Sheet.Root>
		</div>
		
		<div class="hidden lg:block">
			<a href="/">
				<img src={logo} alt="MZ logo" width="60">
			</a>
		</div>

		<div class="flex items-center gap-4">
			<a href="/about-me" class="hidden lg:block">
				<Button variant="ghost">About Me</Button>
			</a>

			<a href="/skills" class="hidden lg:block">
				<Button variant="ghost">My Skills</Button>
			</a>

			<a href="/projects" class="hidden lg:block">
				<Button variant="ghost">Projects</Button>
			</a>

			<a href="/contact" class="hidden lg:block">
				<Button variant="ghost">Contact</Button>
			</a>

			<a href="https://github.com/maliByatzes/" target="_blank">
				<Button variant="ghost">
					<img src={ghLogo} alt="Github logo" width="30">
				</Button>
			</a>
		</div>
	</nav>
</header>

<div class="mt-16 min-h-[800px] w-full overflow-y-hidden">
	<slot />
</div>

<style>
  header {
    box-shadow: 0 0 0 transparent;
    backdrop-filter: blur(50px);
    max-width: 100vw;
    position: fixed;
    top: 0;
    transition: box-shadow .2s ease-in-out;
    width: 100%;
    z-index: 40;
  }
</style>
