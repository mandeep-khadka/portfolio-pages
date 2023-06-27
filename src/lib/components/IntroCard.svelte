<script>
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

	let fullName = 'Mandeep Khadka';
	let width = '250px';
</script>

<div style="width: {width};">
	<Card variant="outlined">
		<PrimaryAction on:click={() => {}}>
			<Media class="profile-photo" aspectRatio="square">
				<MediaContent />
			</Media>
			<Content>
				<div class="mdc-typography--headline5">
					{fullName}
				</div>
			</Content>
		</PrimaryAction>
		<Actions>
			<ActionButtons>
				<Button on:click={() => {}}>
					<Label
						><a href="https://github.com/mak627" target="_blank"
							><i class="fa fa-github fa-3x" style="color:#171515;" /></a
						></Label
					>
				</Button>
				<Button on:click={() => {}}>
					<Label
						><a href="mailto:mandeep.khadka.np@gmail.com"
							><i class="fa fa-envelope fa-3x" style="color:#ea4335;" /></a
						></Label
					>
				</Button>
				<Button on:click={() => {}}>
					<Label
						><a href="https://www.linkedin.com/in/mandeep-khadka/" target="_blank"
							><i class="fa fa-linkedin-square fa-3x" /></a
						></Label
					>
				</Button>
			</ActionButtons>
			<!-- <ActionIcons>
				<IconButton
					on:click={() => clicked++}
					toggle
					aria-label="Add to favorites"
					title="Add to favorites"
				>
					<Icon class="material-icons" on>favorite</Icon>
					<Icon class="material-icons">favorite_border</Icon>
				</IconButton>
				<IconButton class="material-icons" on:click={() => clicked++} title="Share"
					>share</IconButton
				>
				<IconButton class="material-icons" on:click={() => clicked++} title="More options"
					>more_vert</IconButton
				>
			</ActionIcons> -->
		</Actions>
	</Card>
</div>

<style>
	* :global(.profile-photo) {
		background-image: url('/pp.jpg');
		background-size: cover;
	}
</style>
