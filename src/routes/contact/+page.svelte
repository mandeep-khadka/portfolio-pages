<script>
	import PageHeader from '$lib/components/PageHeader.svelte';

	import Card, {
		Content,
		PrimaryAction,
		Media,
		MediaContent,
		Actions,
		ActionButtons,
		ActionIcons
	} from '@smui/card';
	import Button, { Label } from '@smui/button';
	import IconButton, { Icon } from '@smui/icon-button';

	let width = '750px';
</script>

<PageHeader title="Contact" />

<div style="width: {width}; margin: auto;">
	<Card>
		<PrimaryAction on:click={() => clicked++}>
			<Media class="card-media-16x9" aspectRatio="16x9">
				<MediaContent>
					<div style="color: #fff; position: absolute; bottom: 16px; left: 16px;">
						<h2 class="mdc-typography--headline6" style="margin: 0; color:black; font-style:italic">"Jewel Of The Alps", Innsbruck 2022.</h2>
						<h3 class="mdc-typography--subtitle2" style="margin: 0; color:black;">&copy; 2023.</h3>
					</div>
				</MediaContent>
			</Media>
			<Content class="mdc-typography--body1">
				I would love to get in touch.
			</Content>
		</PrimaryAction>
		<Actions>
			<ActionButtons>
				<IconButton class="material-icons" on:click={() => {}}>smartphone</IconButton>
				<Label>01-987654321</Label>
				<IconButton class="material-icons" on:click={() => {}}>mail</IconButton>
				<Label>mandeep.khadka.np@gmail.com</Label>
			</ActionButtons>
			<ActionIcons>
				<!-- <IconButton
					on:click={() => clicked++}
					toggle
					aria-label="Add to favorites"
					title="Add to favorites"
				>
					<Icon class="material-icons" on>favorite</Icon>
					<Icon class="material-icons">favorite_border</Icon>
				</IconButton> -->
				<IconButton class="material-icons" on:click={() => {}} title="Share">share</IconButton>
				<IconButton class="material-icons" on:click={() => {}} title="More options"
					>more_vert</IconButton
				>
			</ActionIcons>
		</Actions>
	</Card>
</div>

<style>
	* :global(.card-media-16x9) {
		background-image: url('/contact-cover.jpg');
	}
</style>
