<script lang="ts">
	export let project: any;

	import Paper, { Title, Content } from '@smui/paper';
</script>

<div class="paper-container" style="margin:10px;">
	<Paper color="secondary" class="mdc-theme--secondary">
		<Title>{project.title}</Title>
		<Content>
			{project.description}
		</Content>
	</Paper>
</div>

<style lang="scss">
	.image {
		max-width: 1400px;
		height: 550px;
		overflow: hidden;
		display: flex;
		justify-content: center;
		background-color: #e9ecef;
	}

	.details {
		display: flex;
		flex-direction: column;
		@media (min-width: 768px) {
			flex-direction: row;
		}
		.project-details {
			flex: 1;
		}
		.description {
			flex: 2;
		}
	}

	img {
		width: 100%;
		height: auto;
		margin-left: auto;
		margin-right: auto;
	}
</style>
