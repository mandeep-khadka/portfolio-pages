<script lang="ts">
	import Project from '$lib/components/Project.svelte';
	import projects from '$lib/data/projects';
	import Button, { Label, Icon } from '@smui/button';
	import IntroCard from '$lib/components/IntroCard.svelte';
	import ProfileDetails from '$lib/components/ProfileDetails.svelte';
	import LayoutGrid, { Cell } from '@smui/layout-grid';
</script>

<LayoutGrid
	style="postion: relative; margin-top: 1%;margin-left: 2px;
border: 3px solid grey;"
>
	<Cell span={3}>
		<div class="cell-adj">
			<IntroCard />
		</div>
	</Cell>
	<Cell span={9}>
		<div>
			<ProfileDetails />
		</div>
	</Cell>
</LayoutGrid>

<section class="skills">
	<div>
		<h3>Skills</h3>
		<p class="subtitle">
			Around 3 years of experience as a software development engineer, familiar using the following
			languages, frameworks and technologies.
		</p>
		<ul class="icons">
			<li>
				<img
					src="https://upload.wikimedia.org/wikipedia/commons/c/c3/Python-logo-notext.svg"
					alt="Python"
				/>
			</li>
			<li>
				<img
					src="https://upload.wikimedia.org/wikipedia/commons/1/18/ISO_C%2B%2B_Logo.svg"
					alt="C++"
				/>
			</li>
			<li>
				<img src="/icons/html.svg" alt="HTML" />
			</li>
			<li>
				<img src="/icons/css.svg" alt="CSS" />
			</li>
			<li>
				<img src="/icons/js.svg" alt="JavaScript" />
			</li>
		</ul>
	</div>
</section>

<section class="projects">
	<div>
		<h3>Projects</h3>
		{#each projects.slice(0, 2) as project}
			<Project {project} />
		{/each}
		<Button href="/projects" target="_blank">
			<Label>More..</Label>
		</Button>
	</div>
</section>

<section class="socials">
	<h4>Follow Me On</h4>
	<!-- <p>I would love to connect with you.</p> -->
	<div class="links">
		<!-- <a href="https://github.com/mak627" target="_blank"><i class="fa fa-github fa-3x" style="color:#171515;"></i></a> -->
		<!-- <a href="https://www.linkedin.com/in/mandeep-khadka/" target="_blank"
			><i class="fa fa-linkedin-square fa-3x" /></a
		> -->
		<a href="https://www.instagram.com//__man_in_deep/" target="_blank"
			><i class="fa fa-instagram fa-3x" style="color:red" /></a
		>
		<a href="https://twitter.com/man_deep27" target="_blank"><i class="fa fa-twitter fa-3x" /></a>
		<!-- <a href="mailto:mandeep.khadka.np@gmail.com"><i class="fa fa-envelope fa-3x" style="color:#ea4335;"></i></a> -->
	</div>
</section>

<style lang="scss">
	section {
		display: flex;
		align-items: center;
		justify-content: center;
	}

	.subtitle {
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
	}

	.profile {
		width: 100%;
		height: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		background-color: red;
	}

	.skills,
	.socials {
		text-align: center;
		display: flex;
		align-items: center;
		justify-content: center;
		flex-direction: column;
		padding: 40px;
		ul {
			list-style: none;
			margin: 0;
			padding: 0;
			display: flex;
			justify-content: center;
			li {
				margin-left: 10px;
			}
			img {
				width: 48px;
				height: 48px;
			}
		}
	}

	.projects {
		text-align: center;
		display: flex;
		flex-direction: column;
		align-items: center;
		justify-content: center;
	}

	.links {
		a {
			margin-left: 8px;
			display: inline-block;
			padding: 8px;
		}
	}

	.cell-adj {
		display: flex;
		height: -256px;
		padding: 4.5% 0% 0 20%;
	}
</style>
